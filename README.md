# Singleton-Design-Pattern

    // we need first of all to create the singlton instance that will be used alwayes
    // it will be a static private type
    // it will be equal null at the begining because I need to detect it it is created as opject or not to use on the getInstance method

    private  static SwingCalendar instance = null;
    
    // here I will do the method that if used will return the instance opject as per the singleton pattern
    // which is getInstance that will create an object if it is the first time calling the method and will return it
    // else it will return the already created opject
    public static SwingCalendar getInstance(){
        if(instance == null){
            instance = new SwingCalendar();
        }
        return  instance;
    }
    
    
    /**
     * Create and show new calender object
     * Todo: This method logs the object HashCode in a text file, after refactoring the code; show warning message if the HashCode of Calender1 doesn't equal Calender2 HashCode
     */
    private void showNewCalender() {
        SwingCalendar sc;
        sc = SwingCalendar.getInstance();
        Util.Logger.log("Object HC: " + sc.hashCode()); // Log Calender hash code

    }
