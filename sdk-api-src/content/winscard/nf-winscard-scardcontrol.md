---
UID: NF:winscard.SCardControl
title: SCardControl function
author: windows-driver-content
description: Gives you direct control of the reader. You can call it any time after a successful call to SCardConnect and before a successful call to SCardDisconnect.
old-location: security\scardcontrol.htm
old-project: SecAuthN
ms.assetid: e8c69e61-4e5e-4385-a0f1-9b594c479984
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SCardControl, SCardControl function [Security], _smart_scardcontrol, security.scardcontrol, winscard/SCardControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
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
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winscard.dll
api_name:
-	SCardControl
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardControl function


## -description


The <b>SCardControl</b> function gives you direct control of the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>. You can call it any time after a successful call to <a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> and before a successful call to <a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>. The effect on the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the reader depends on the control code.


## -parameters




### -param hCard [in]

Reference value returned from 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


### -param dwControlCode [in]

Control code for the operation. This value identifies the specific operation to be performed.


### -param lpInBuffer [in]

Pointer to a buffer that contains the data required to perform the operation. This parameter can be <b>NULL</b> if the <i>dwControlCode</i> parameter specifies an operation that does not require input data.


### -param cbInBufferSize

TBD


### -param lpOutBuffer [out]

Pointer to a buffer that receives the operation's output data. This parameter can be <b>NULL</b> if the <i>dwControlCode</i> parameter specifies an operation that does not produce output data.


### -param cbOutBufferSize

TBD


### -param lpBytesReturned [out]

Pointer to a <b>DWORD</b> that receives the size, in bytes, of the data stored into the buffer pointed to by <i>lpOutBuffer</i>.


#### - nInBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpInBuffer</i>.


#### - nOutBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpOutBuffer</i>. 


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>SCardControl</b> function is a direct card access function. For more information on other direct access functions, see 
<a href="https://msdn.microsoft.com/ea6cfa5a-2abf-4b7f-b3f4-99655266f030">Direct Card Access Functions</a>.


#### Examples

The following example issues a control code. The example assumes that hCardHandle is a valid handle received from a previous call to <a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> and that dwControlCode is a variable of type <b>DWORD</b> previously initialized to a valid control code. This particular control code requires no input data and expects no output data.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardControl( hCardHandle,
                        dwControlCode,
                        NULL,
                        0,
                        NULL,
                        0,
                        0 );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardControl\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>
 

 

