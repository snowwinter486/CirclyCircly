CirclyCircly
============
import java.awt.Graphics;
import java.awt.Color;
import javax.swing.JFrame;
import javax.swing.JComponent;
import java.awt.Font;
import java.awt.FontMetrics;
import java.awt.Transparency;
/**
 *Circle w/ your choice of color
 *Write "This Group" within circle
 * Two more circles on downward angle from 1st circle
 * Circle 1 = "Gym." 
 * Circle 2 = "English"
 * Circle 3 = "Math"
 * @Su-Ah L + Fredrick O
 * @version (2.0)
 */
public class CirclyCircly
{
   public static void draw(Graphics g)
    { 
     Color Teal = new Color(0, 128, 192);
     Color Black = new Color(0, 0, 0);
     Color Maroon = new Color(136, 0, 21);
     Color Lavi = new Color(200, 191, 231);
     //g.setColor(Teal);
     //g.drawOval(60, 30, 200, 200);
     g.setColor(Maroon);
     g.drawOval(150, 150, 200, 200);
     g.setColor(Lavi);
     g.drawOval(20, 150, 200, 200);
     g.setColor(Black);
     FontMetrics fm = g.getFontMetrics();
     //g.drawString("Gym", 70, 90);
     g.drawString("Trying", 40, 220);
     g.drawString("Learning", 250, 230);
    }   
    public static void main(String[] args)
   {  
      JFrame frame = new JFrame();  
      final int FRAME_WIDTH = 400;
      final int FRAME_HIGHT = 400;     
      frame.setSize(FRAME_WIDTH, FRAME_HIGHT);
      frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
      JComponent component = new JComponent()
        {  public void paintComponent(Graphics graph)
          { 
            draw(graph); 
          } 
        };
      frame.add(component);
      frame.setVisible(true); 
   }  
    }
