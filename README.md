# accuracy_report

Accuracy reports reads to input sources:

1. Generate reality output with incidences :
  - matrix_data_manager  https://github.com/Glovo/matrix_data_manager
  - stored in folder reality_data
  
      dwh_data = rdetl.get_reality_observed(MC, DC)
    incidences, incidences_summary = rdetl.get_reality_incidences(MC, DC)

    output_folder_path = "/Users/angelikastanke/projects/accuracy_report/reality_data/"

    dwh_data.to_csv(output_folder_path  + "%s_%s_%s.csv" %(MC.city, MC.start_date, MC.end_date))
    incidences.to_csv(output_folder_path  + "incidences_orders_%s_%s_%s.csv" %(MC.city, MC.start_date, MC.end_date), index=False)
    incidences_summary.to_csv(output_folder_path  + "incidences_summary_%s_%s_%s.csv" %(MC.city, MC.start_date, MC.end_date), index=False)

2. Generate simulation output
  - dispatching_simulator https://github.com/Glovo/dispatching-simulator
  - stored in folder reality_data
  
  output_folder_path = "/Users/angelikastanke/projects/accuracy_report/simulator_output/"
  output_file_name = "orders_times_%s_%s_%s.csv" %(MC.city, MC.start_date, MC.end_date)
  orders_times.to_csv(output_folder_path + output_file_name)
  
  
