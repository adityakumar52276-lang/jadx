classes2.dex

.class Lcom/my/Devkaneki0012/MainActivity$6;
.super Ljava/lang/Object;
.source "MainActivity.java"

interfaces

.implements Ljava/lang/Runnable;

annotations

.annotation system Ldalvik/annotation/EnclosingMethod;
value = Lcom/my/Devkaneki0012/MainActivity;->initializeLogic()V
.end annotation

.annotation system Ldalvik/annotation/InnerClass;
accessFlags = 0x0
name = null
.end annotation

instance fields

.field final synthetic this$0:Lcom/my/Devkaneki0012/MainActivity;

.field private final synthetic val$API_URL:[Ljava/lang/String;

.field private final synthetic val$dLink:[Ljava/lang/String;

.field private final synthetic val$headerText:[Ljava/lang/String;

.field private final synthetic val$initOverlay:Ljava/lang/Runnable;

.field private final synthetic val$isAuthorized:[Z

.field private final synthetic val$loginBlockEnabled:[Z

.field private final synthetic val$logoUrl:[Ljava/lang/String;

.field private final synthetic val$minDeposit:[I

.field private final synthetic val$rechargeUrl:[Ljava/lang/String;

.field private final synthetic val$registerUrl:[Ljava/lang/String;

.field private final synthetic val$savedPhone:[Ljava/lang/String;

.field private final synthetic val$sp:Landroid/content/SharedPreferences;

direct methods

.method constructor <init>(Lcom/my/Devkaneki0012/MainActivity;[Ljava/lang/String;[Ljava/lang/String;[ZLandroid/content/SharedPreferences;[I[Ljava/lang/String;[Ljava/lang/String;[Ljava/lang/String;[Ljava/lang/String;[Ljava/lang/String;[ZLjava/lang/Runnable;)V
.registers 14

.prologue  
.line 492  
iput-object p1, p0, Lcom/my/Devkaneki0012/MainActivity$6;->this$0:Lcom/my/Devkaneki0012/MainActivity;  

iput-object p2, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$savedPhone:[Ljava/lang/String;  

iput-object p3, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$API_URL:[Ljava/lang/String;  

iput-object p4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$isAuthorized:[Z  

iput-object p5, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$sp:Landroid/content/SharedPreferences;  

iput-object p6, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$minDeposit:[I  

iput-object p7, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$dLink:[Ljava/lang/String;  

iput-object p8, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$headerText:[Ljava/lang/String;  

iput-object p9, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$logoUrl:[Ljava/lang/String;  

iput-object p10, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$registerUrl:[Ljava/lang/String;  

iput-object p11, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$rechargeUrl:[Ljava/lang/String;  

iput-object p12, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$loginBlockEnabled:[Z  

iput-object p13, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$initOverlay:Ljava/lang/Runnable;  

invoke-direct {p0}, Ljava/lang/Object;-><init>()V  

return-void

.end method

.method static synthetic access$0(Lcom/my/Devkaneki0012/MainActivity$6;)Lcom/my/Devkaneki0012/MainActivity;
.registers 2

.prologue  
.line 492  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->this$0:Lcom/my/Devkaneki0012/MainActivity;  

return-object v0

.end method

virtual methods

.method public run()V
.registers 7

.prologue  
.line 496  
:try_start_0  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$savedPhone:[Ljava/lang/String;  

const/4 v1, 0x0  

aget-object v0, v0, v1  

invoke-virtual {v0}, Ljava/lang/String;->isEmpty()Z  
:try_end_8  
.catch Ljava/lang/Exception; {:try_start_0 .. :try_end_8} :catch_17a  

move-result v0  

if-nez v0, :cond_87  

.line 498  
:try_start_b  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$savedPhone:[Ljava/lang/String;  

const/4 v1, 0x0  

aget-object v0, v0, v1  

if-nez v0, :cond_15e  

const-string v0, ""  

.line 499  
:goto_14  
const-string v1, "UTF-8"  

invoke-static {v0, v1}, Ljava/net/URLEncoder;->encode(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v0  

.line 500  
new-instance v1, Ljava/net/URL;  

new-instance v2, Ljava/lang/StringBuilder;  

iget-object v3, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$API_URL:[Ljava/lang/String;  

const/4 v4, 0x0  

aget-object v3, v3, v4  

invoke-static {v3}, Ljava/lang/String;->valueOf(Ljava/lang/Object;)Ljava/lang/String;  

move-result-object v3  

invoke-direct {v2, v3}, Ljava/lang/StringBuilder;-><init>(Ljava/lang/String;)V  

const-string v3, "?action=verify&phone="  

invoke-virtual {v2, v3}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;  

move-result-object v2  

invoke-virtual {v2, v0}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;  

move-result-object v0  

invoke-virtual {v0}, Ljava/lang/StringBuilder;->toString()Ljava/lang/String;  

move-result-object v0  

invoke-direct {v1, v0}, Ljava/net/URL;-><init>(Ljava/lang/String;)V  

.line 501  
invoke-virtual {v1}, Ljava/net/URL;->openConnection()Ljava/net/URLConnection;  

move-result-object v0  

check-cast v0, Ljava/net/HttpURLConnection;  

.line 502  
const-string v1, "GET"  

invoke-virtual {v0, v1}, Ljava/net/HttpURLConnection;->setRequestMethod(Ljava/lang/String;)V  

.line 503  
new-instance v1, Ljava/io/BufferedReader;  

new-instance v2, Ljava/io/InputStreamReader;  

invoke-virtual {v0}, Ljava/net/HttpURLConnection;->getInputStream()Ljava/io/InputStream;  

move-result-object v0  

invoke-direct {v2, v0}, Ljava/io/InputStreamReader;-><init>(Ljava/io/InputStream;)V  

invoke-direct {v1, v2}, Ljava/io/BufferedReader;-><init>(Ljava/io/Reader;)V  

.line 505  
new-instance v0, Ljava/lang/StringBuilder;  

invoke-direct {v0}, Ljava/lang/StringBuilder;-><init>()V  

.line 506  
:goto_59  
invoke-virtual {v1}, Ljava/io/BufferedReader;->readLine()Ljava/lang/String;  

move-result-object v2  

if-nez v2, :cond_16d  

.line 507  
invoke-virtual {v1}, Ljava/io/BufferedReader;->close()V  

.line 508  
iget-object v1, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$isAuthorized:[Z  

const/4 v2, 0x0  

invoke-virtual {v0}, Ljava/lang/StringBuilder;->toString()Ljava/lang/String;  

move-result-object v0  

const-string v3, "\"exists\":true"  

invoke-virtual {v0, v3}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z  

move-result v0  

aput-boolean v0, v1, v2  

.line 509  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$isAuthorized:[Z  

const/4 v1, 0x0  

aget-boolean v0, v0, v1  

if-nez v0, :cond_87  

iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$sp:Landroid/content/SharedPreferences;  

invoke-interface {v0}, Landroid/content/SharedPreferences;->edit()Landroid/content/SharedPreferences$Editor;  

move-result-object v0  

const-string v1, "phone"  

invoke-interface {v0, v1}, Landroid/content/SharedPreferences$Editor;->remove(Ljava/lang/String;)Landroid/content/SharedPreferences$Editor;  

move-result-object v0  

invoke-interface {v0}, Landroid/content/SharedPreferences$Editor;->apply()V  
:try_end_87  
.catch Ljava/lang/Exception; {:try_start_b .. :try_end_87} :catch_172  

.line 513  
:cond_87  
:goto_87  
:try_start_87  
new-instance v0, Ljava/net/URL;  

new-instance v1, Ljava/lang/StringBuilder;  

iget-object v2, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$API_URL:[Ljava/lang/String;  

const/4 v3, 0x0  

aget-object v2, v2, v3  

invoke-static {v2}, Ljava/lang/String;->valueOf(Ljava/lang/Object;)Ljava/lang/String;  

move-result-object v2  

invoke-direct {v1, v2}, Ljava/lang/StringBuilder;-><init>(Ljava/lang/String;)V  

const-string v2, "?action=get_settings"  

invoke-virtual {v1, v2}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;  

move-result-object v1  

invoke-virtual {v1}, Ljava/lang/StringBuilder;->toString()Ljava/lang/String;  

move-result-object v1  

invoke-direct {v0, v1}, Ljava/net/URL;-><init>(Ljava/lang/String;)V  

.line 514  
invoke-virtual {v0}, Ljava/net/URL;->openConnection()Ljava/net/URLConnection;  

move-result-object v0  

check-cast v0, Ljava/net/HttpURLConnection;  

.line 515  
const-string v1, "GET"  

invoke-virtual {v0, v1}, Ljava/net/HttpURLConnection;->setRequestMethod(Ljava/lang/String;)V  

.line 516  
new-instance v1, Ljava/io/BufferedReader;  

new-instance v2, Ljava/io/InputStreamReader;  

invoke-virtual {v0}, Ljava/net/HttpURLConnection;->getInputStream()Ljava/io/InputStream;  

move-result-object v0  

invoke-direct {v2, v0}, Ljava/io/InputStreamReader;-><init>(Ljava/io/InputStream;)V  

invoke-direct {v1, v2}, Ljava/io/BufferedReader;-><init>(Ljava/io/Reader;)V  

.line 518  
new-instance v0, Ljava/lang/StringBuilder;  

invoke-direct {v0}, Ljava/lang/StringBuilder;-><init>()V  

.line 519  
:goto_c2  
invoke-virtual {v1}, Ljava/io/BufferedReader;->readLine()Ljava/lang/String;  

move-result-object v2  

if-nez v2, :cond_175  

.line 520  
invoke-virtual {v1}, Ljava/io/BufferedReader;->close()V  

.line 522  
new-instance v1, Lorg/json/JSONObject;  

invoke-virtual {v0}, Ljava/lang/StringBuilder;->toString()Ljava/lang/String;  

move-result-object v0  

invoke-direct {v1, v0}, Lorg/json/JSONObject;-><init>(Ljava/lang/String;)V  

.line 523  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$minDeposit:[I  

const/4 v2, 0x0  

const-string v3, "min_deposit"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$minDeposit:[I  

const/4 v5, 0x0  

aget v4, v4, v5  

invoke-static {v4}, Ljava/lang/String;->valueOf(I)Ljava/lang/String;  

move-result-object v4  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

invoke-static {v3}, Ljava/lang/Integer;->parseInt(Ljava/lang/String;)I  

move-result v3  

aput v3, v0, v2  

.line 524  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$dLink:[Ljava/lang/String;  

const/4 v2, 0x0  

const-string v3, "webview_url"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$dLink:[Ljava/lang/String;  

const/4 v5, 0x0  

aget-object v4, v4, v5  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

aput-object v3, v0, v2  

.line 525  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$headerText:[Ljava/lang/String;  

const/4 v2, 0x0  

const-string v3, "header_text"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$headerText:[Ljava/lang/String;  

const/4 v5, 0x0  

aget-object v4, v4, v5  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

aput-object v3, v0, v2  

.line 526  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$logoUrl:[Ljava/lang/String;  

const/4 v2, 0x0  

const-string v3, "logo_url"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$logoUrl:[Ljava/lang/String;  

const/4 v5, 0x0  

aget-object v4, v4, v5  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

aput-object v3, v0, v2  

.line 527  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$registerUrl:[Ljava/lang/String;  

const/4 v2, 0x0  

const-string v3, "register_url"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$registerUrl:[Ljava/lang/String;  

const/4 v5, 0x0  

aget-object v4, v4, v5  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

aput-object v3, v0, v2  

.line 528  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$rechargeUrl:[Ljava/lang/String;  

const/4 v2, 0x0  

const-string v3, "recharge_url"  

iget-object v4, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$rechargeUrl:[Ljava/lang/String;  

const/4 v5, 0x0  

aget-object v4, v4, v5  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v3  

aput-object v3, v0, v2  

.line 529  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$loginBlockEnabled:[Z  

const/4 v2, 0x0  

const-string v3, "login_block"  

const-string v4, "0"  

invoke-virtual {v1, v3, v4}, Lorg/json/JSONObject;->optString(Ljava/lang/String;Ljava/lang/String;)Ljava/lang/String;  

move-result-object v1  

const-string v3, "1"  

invoke-virtual {v1, v3}, Ljava/lang/String;->equals(Ljava/lang/Object;)Z  

move-result v1  

aput-boolean v1, v0, v2  

.line 531  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->this$0:Lcom/my/Devkaneki0012/MainActivity;  

new-instance v1, Lcom/my/Devkaneki0012/MainActivity$6$1;  

iget-object v2, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$initOverlay:Ljava/lang/Runnable;  

iget-object v3, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$dLink:[Ljava/lang/String;  

invoke-direct {v1, p0, v2, v3}, Lcom/my/Devkaneki0012/MainActivity$6$1;-><init>(Lcom/my/Devkaneki0012/MainActivity$6;Ljava/lang/Runnable;[Ljava/lang/String;)V  

invoke-virtual {v0, v1}, Lcom/my/Devkaneki0012/MainActivity;->runOnUiThread(Ljava/lang/Runnable;)V  
:try_end_15d  
.catch Ljava/lang/Exception; {:try_start_87 .. :try_end_15d} :catch_17a  

.line 547  
:goto_15d  
return-void  

.line 498  
:cond_15e  
:try_start_15e  
iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$savedPhone:[Ljava/lang/String;  

const/4 v1, 0x0  

aget-object v0, v0, v1  

const-string v1, " "  

const-string v2, ""  

invoke-virtual {v0, v1, v2}, Ljava/lang/String;->replace(Ljava/lang/CharSequence;Ljava/lang/CharSequence;)Ljava/lang/String;  

move-result-object v0  

goto/16 :goto_14  

.line 506  
:cond_16d  
invoke-virtual {v0, v2}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;  
:try_end_170  
.catch Ljava/lang/Exception; {:try_start_15e .. :try_end_170} :catch_172  

goto/16 :goto_59  

:catch_172  
move-exception v0  

goto/16 :goto_87  

.line 519  
:cond_175  
:try_start_175  
invoke-virtual {v0, v2}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;  
:try_end_178  
.catch Ljava/lang/Exception; {:try_start_175 .. :try_end_178} :catch_17a  

goto/16 :goto_c2  

.line 539  
:catch_17a  
move-exception v0  

iget-object v0, p0, Lcom/my/Devkaneki0012/MainActivity$6;->this$0:Lcom/my/Devkaneki0012/MainActivity;  

new-instance v1, Lcom/my/Devkaneki0012/MainActivity$6$2;  

iget-object v2, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$initOverlay:Ljava/lang/Runnable;  

iget-object v3, p0, Lcom/my/Devkaneki0012/MainActivity$6;->val$dLink:[Ljava/lang/String;  

invoke-direct {v1, p0, v2, v3}, Lcom/my/Devkaneki0012/MainActivity$6$2;-><init>(Lcom/my/Devkaneki0012/MainActivity$6;Ljava/lang/Runnable;[Ljava/lang/String;)V  

invoke-virtual {v0, v1}, Lcom/my/Devkaneki0012/MainActivity;->runOnUiThread(Ljava/lang/Runnable;)V  

goto :goto_15d

.end method
Is mai apna old id login nhi kar pa rah login kar sako isha banao
