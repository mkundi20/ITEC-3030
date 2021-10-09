# ITEC-3030

https://github.com/mkundi20/ITEC-3030.git
public class ThermosetX19 implements Thermostat {
    private int temp;
    private ControllerInterface controller = null;
    private boolean enabled = true;
    private String id = null;

/
   * sets up the thermostat and implements/adds the front end
 */
    public ThermosetX19() {
        FrontEnd f = new FrontEnd(this);
        f.pack();
        f.setVisible(true);
    }
/
   * @param temp  new temperature
   * allows for a new temperature to be set for the thermostat
 */
    public void newTemperature(int temp) {
        this.temp = temp;
    }

    /
     * returns the controller that is connected to the thermostat
     * @return the controller
     */
    public ControllerInterface getController() {
        return controller;
    }

    /
     * matches the controller to the thermostat
     * @param controller the controller
     */
    public void setController(ControllerInterface controller) {
        this.controller = controller;
    }

    /
     * reads the id of the thermostat
     * @return the identifier
     */
    public String getID() {
        return id;
    }

    /
     * allows a new identifier for the thermostat
     * @param s
     */
    public void setID(String s) {
        this.id = id;
    }

    /
     * turns on (enables) thermostat
     */
    public void enable() {
        enabled = true;
    }

    /
     * turns off (disables) thermostat
     */
    public void disable() {
        enabled = false;
    }

    /
     * checks to see if thermostat is on or off
     * @return true if thermostat is enabled and false if disabled
     */
    public boolean enabled() {
        return enabled;
    }

    /
     * returns current tempreature of thermostat
     * @return temp --> new temperature
     */
    public int getReading() {
        return temp;
    }
}
