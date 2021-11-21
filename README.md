# Hello_world
Just a begining
import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.Date;

public class helloworld {
    public static void main(String[] args) throws ParseException {
        paneltyfunc("2020-09-08","2020-09-15");
    }
        public static int paneltyfunc (String date1, String date2)throws ParseException{
//             date1 = "2020-09-08";
//             date2 = "2020-09-15";
            int panelty;
            SimpleDateFormat formatter = new SimpleDateFormat("yyyy-mm-dd");
            Date returndate = formatter.parse(date1);
            Date extendeddate = formatter.parse(date2);
            long difference_In_Time = extendeddate.getTime() - returndate.getTime();
            if (returndate.before(extendeddate)) {
                long difference_In_Days = (difference_In_Time / (1000 * 60 * 60 * 24)) % 365;
                panelty = (int) (difference_In_Days * 2);
                System.out.println("........."+panelty);
            } else {
                panelty = 0;
            }
            return panelty;
        }
    }
