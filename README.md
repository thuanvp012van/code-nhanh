Chu kì cứ mỗi 1 tuần mình lại update 1 hay nhiều phím tắt mới nhé
rq : Request $rq
!empty : if(!empty(gi_do))
		 {
			 #code
		 }


!isset : if(!isset(gi_do))
		 {
			 #code
		 }


empty : if(empty(gi_do))
        {
            #code
        }

isset : if(isset(gi_do))
        {
            #code
        }

checkLogin : Auth::guard('')->attempt(['email' => $rq->email, 'password' => $rq->password], $rq->get('remember'))  **thu vien auth**

getSession : Auth::guard('')->user() **thu vien auth**


colinteger : $table->integer('votes')->unsigned()->nullable()->default(12);

colforeign : $table->foreign('user_id')->references('id')->on('users')->onDelete('cascade');

colstring : $table->string('name', 100)->nullable()->default('text');

colchar : $table->char('name', 4)->default('text');

coldate : $table->date('created_at')->nullable()->default({new DateTime());

coltext : $table->text('description')->nullable()->default('text');

colfloat : $table->float('amount')->nullable()->default(123.45);

colboolean : $table->boolean('confirmed')->nullable()->default(false);

colincrements : $table->increments('id');

colbigIncrements : $table->bigIncrements('id');

coltinyInteger : $table->tinyInteger('numbers');

colrememberToken : $table->rememberToken();

coldateTime : $table->dateTime('created_at')->nullable()->default(new DateTime());
