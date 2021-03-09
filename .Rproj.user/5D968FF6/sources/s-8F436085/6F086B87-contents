myapp <- function() {
  library(heatdata)
  shiny::shinyApp(
    ui = shiny::fluidPage(
      shiny::numericInput("n", "n", 1),
      shiny::plotOutput("plot"),
      shiny::tableOutput("table")
    ),
    server = function(input, output) {
      output$plot <- shiny::renderPlot( plot(head(cars, input$n)) )
      output$table <- shiny::renderTable(heatdata::data_heat_strata[1:3,])
    }
  )
}
