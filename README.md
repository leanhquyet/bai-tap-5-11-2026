# bai-tap-5-11-2026
using System;

namespace ClinicAppointmentManager
{
    public enum AppointmentStatus
    {
        ChoKham,
        DangKham,
        HoanTat,
        DaHuy
    }

    public class Appointment
    {
        public string Id { get; set; }
        public string PatientName { get; set; }
        public string PhoneNumber { get; set; }
        public DateTime AppointmentDate { get; set; }
        public string DoctorName { get; set; }
        public string Reason { get; set; }
        public AppointmentStatus Status { get; set; }

        public string StatusDisplay
        {
            get
            {
                switch (Status)
                {
                    case AppointmentStatus.ChoKham: return "Chờ khám";
                    case AppointmentStatus.DangKham: return "Đang khám";
                    case AppointmentStatus.HoanTat: return "Hoàn tất";
                    case AppointmentStatus.DaHuy: return "Đã hủy";
                    default: return "";
                }
            }
        }
    }
}
