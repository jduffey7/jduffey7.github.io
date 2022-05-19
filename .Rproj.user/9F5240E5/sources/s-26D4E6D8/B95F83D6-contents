library(shiny)
ui <- fluidPage(
  
  h2(textOutput("currentTime"))
  
)

# Define server logic to show current time, update every second ----
server <- function(input, output, session) {
  
  output$currentTime <- renderText({
    invalidateLater(1000, session)
    paste("The current date is", Sys.Date())
  })
  
}

# Create Shiny app ----
shinyApp(ui, server)