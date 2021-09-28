int cols, rows;
int scl=11;
int w=600;
int h=600;

float [] [] terrain;


void setup(){
  
  size(900, 900, P3D); 
  cols=w/scl;
  rows=h/scl;
  terrain= new float [cols][rows];
  
  float yoff=0;
  for(int y=0; y<cols; y++){
    float xoff=0;
    for(int x=0; x<rows; x++){
      terrain[x][y]=map(noise(xoff,yoff),0,1,-100,100);
      //terrain[x][y]=random(-10,10);
      xoff+=0.1;
    }
    yoff+=0.1;
  }
  print("hola jeje");
}
void draw(){
  
  background(255);
  stroke(0);
  noFill();
  
  translate(width/2, height/2);
  rotateX(PI/3);
  translate(-w/2, -h/2);
  
  
  
  for(int y=0; y<cols-1; y++){
    beginShape(TRIANGLE_STRIP);
    for(int x=0; x<rows; x++){
    vertex(x*scl, y*scl, terrain[x][y]);
    vertex(x*scl, (y+1)*scl, terrain[x][y+1]);
      
    }
    endShape();
  }
}
