# Credit-card-ETL-Project

Các file theo kiến trúc từng giai đoạn:

- kafka_producer.py: kafka sẽ lấy dữ liệu từ file csv giả lập ngẫu nhiên 1 đến 3s
- spark_hdfs.py: lấy dữ liệu từ kafka và tiến hành các bước transform, sau đó lưu trữ dữ liệu lên hdfs mỗi 60 phút một lần
- create_transaction_file: tạo 1 file tổng chứa header để merge
- merge_data: merge các file đã push hdfs thành 1 file tổng khi chạy, dự kiến file sẽ được chạy vào cuối ngày
- report: powerBI dashboard lấy dữ liệu từ hdfs và thống kê theo yêu cầu
