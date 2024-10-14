# Auction
heres the link to the apk file - https://drive.google.com/file/d/169jshzCe_EuhjrYMat3IKJOHNO-hAK03/view?usp=sharing
module Counter_4bit (
    input clk,
    input reset,
    input enable,
    output reg [3:0] count
);
    always @(posedge clk or posedge reset) begin
        if (reset) begin
            count <= 4'd0;
        end else if (enable) begin
            count <= count + 4'd1;
        end
    end
endmodule
module DFF (
    input D,    // Data input
    input clk,  // Clock signal
    input reset, // Reset signal
    input enable, // Enable signal
    output reg Q  // Output of flip-flop
);
    always @(posedge clk or posedge reset) begin
        if (reset) begin
            Q <= 1'b0;
        end else if (enable) begin
            Q <= D;
        end
    end
endmodule
