(* Signature for expressions in x and y.
   Based on code by Kurt M. Dresner and Chris Stone
*)


module type EXPR =

  sig
    type expr           (* type of expressions *)

    (* Expression creation *)
    (* All expressions should return float values in the range [-1,1]
       when x and y also range over [-1,1]. *)

    val buildX      : expr          (* returns the expression for "x" *)
    val buildY      : expr          (* returns the expression for "y" *)

    val buildSin    : expr -> expr  (* creates sine (PI * given expr) *)
    val buildCos    : expr -> expr  (* creates cosine (PI * given expr) *)

    val buildAvg    : expr * expr -> expr  (* average of the two exprs. *)
    val buildTimes  : expr * expr -> expr  (* product of the two exprs. *)


    (* Produce a string representation of an expression *)
    val exprToString : expr -> string

    (* Expression evaluation *)
    val eval : expr -> float*float -> float

    (* A sample reasonably complicated expression *)
    val sampleExpr : expr

  end
