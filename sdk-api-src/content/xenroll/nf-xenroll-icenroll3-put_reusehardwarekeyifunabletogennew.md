---
UID: NF:xenroll.ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew
title: ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew method
author: windows-driver-content
description: Sets or retrieves a Boolean value that determines the action taken by the certificate enrollment control object if an error is encountered when generating a new key.
old-location: security\icenroll4_reusehardwarekeyifunabletogennew.htm
old-project: SecCrypto
ms.assetid: 5a9d5f78-bf88-4e24-9685-7c504f9f2e38
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CEnroll object [Security], ReuseHardwareKeyIfUnableToGenNew property, ICEnroll3, ICEnroll3 interface [Security], ReuseHardwareKeyIfUnableToGenNew property, ICEnroll3.ReuseHardwareKeyIfUnableToGenNew, ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew, ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew, ICEnroll4 interface [Security], ReuseHardwareKeyIfUnableToGenNew property, ICEnroll4.ReuseHardwareKeyIfUnableToGenNew, ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew, ReuseHardwareKeyIfUnableToGenNew property [Security], ReuseHardwareKeyIfUnableToGenNew property [Security], CEnroll object, ReuseHardwareKeyIfUnableToGenNew property [Security], ICEnroll3 interface, ReuseHardwareKeyIfUnableToGenNew property [Security], ICEnroll4 interface, put_ReuseHardwareKeyIfUnableToGenNew,ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew, security.icenroll4_reusehardwarekeyifunabletogennew, xenroll/ICEnroll3::ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	ICEnroll4.ReuseHardwareKeyIfUnableToGenNew
-	ICEnroll4.get_ReuseHardwareKeyIfUnableToGenNew
-	ICEnroll4.put_ReuseHardwareKeyIfUnableToGenNew
-	ICEnroll3.ReuseHardwareKeyIfUnableToGenNew
-	ICEnroll3.get_ReuseHardwareKeyIfUnableToGenNew
-	ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew
-	CEnroll.ReuseHardwareKeyIfUnableToGenNew
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew method


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ReuseHardwareKeyIfUnableToGenNew</b> property sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

This property was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

This property is read/write.


## -parameters


## -remarks



This property is a Boolean value. This property affects only <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> that return NTE_TOKEN_KEYSET_STORAGE_FULL. These CSPs are typically hardware-based; an example is a smart card. If this property is true and an error is encountered while generating a new key, the certificate enrollment control object will reuse the existing hardware key. If this property is false and an error is encountered while generating a new key, the certificate enrollment control object will not reuse the existing hardware key but will instead pass an error to the caller.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Code to set the reuse H/W key status.
// hr is HRESULT variable.
hr = pEnroll-&gt;put_ReuseHardwareKeyIfUnableToGenNew( FALSE );
if ( FAILED( hr ) )    
    printf("Failed put_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);


// Code to retrieve the reuse H/W key status.
BOOL bReuse;

hr = pEnroll-&gt;get_ReuseHardwareKeyIfUnableToGenNew( &amp;bReuse );
if ( FAILED( hr ) )
    printf("Failed get_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);
else
    printf("Hardware key %s be reused if unable"
        " to generate a new key.\n", bReuse ? "will" : "will not");</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

