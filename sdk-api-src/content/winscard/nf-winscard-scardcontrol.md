---
UID: NF:winscard.SCardControl
title: SCardControl function (winscard.h)
description: Gives you direct control of the reader. You can call it any time after a successful call to SCardConnect and before a successful call to SCardDisconnect.
helpviewer_keywords: ["SCardControl","SCardControl function [Security]","_smart_scardcontrol","security.scardcontrol","winscard/SCardControl"]
old-location: security\scardcontrol.htm
tech.root: security
ms.assetid: e8c69e61-4e5e-4385-a0f1-9b594c479984
ms.date: 12/05/2018
ms.keywords: SCardControl, SCardControl function [Security], _smart_scardcontrol, security.scardcontrol, winscard/SCardControl
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardControl
 - winscard/SCardControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardControl
---

# SCardControl function


## -description

The <b>SCardControl</b> function gives you direct control of the <a href="/windows/desktop/SecGloss/r-gly">reader</a>. You can call it any time after a successful call to <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> and before a successful call to <a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>. The effect on the <a href="/windows/desktop/SecGloss/s-gly">state</a> of the reader depends on the control code.

## -parameters

### -param hCard [in]

Reference value returned from 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param dwControlCode [in]

Control code for the operation. This value identifies the specific operation to be performed.

### -param lpInBuffer [in]

Pointer to a buffer that contains the data required to perform the operation. This parameter can be <b>NULL</b> if the <i>dwControlCode</i> parameter specifies an operation that does not require input data.

### -param cbInBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpInBuffer</i>.

### -param lpOutBuffer [out]

Pointer to a buffer that receives the operation's output data. This parameter can be <b>NULL</b> if the <i>dwControlCode</i> parameter specifies an operation that does not produce output data.

### -param cbOutBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>lpOutBuffer</i>.

### -param lpBytesReturned [out]

Pointer to a <b>DWORD</b> that receives the size, in bytes, of the data stored into the buffer pointed to by <i>lpOutBuffer</i>.

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
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

The <b>SCardControl</b> function is a direct card access function. For more information on other direct access functions, see 
<a href="/windows/desktop/SecAuthN/direct-card-access-functions">Direct Card Access Functions</a>.


#### Examples

The following example issues a control code. The example assumes that hCardHandle is a valid handle received from a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> and that dwControlCode is a variable of type <b>DWORD</b> previously initialized to a valid control code. This particular control code requires no input data and expects no output data.


```cpp

lReturn = SCardControl( hCardHandle,
                        dwControlCode,
                        NULL,
                        0,
                        NULL,
                        0,
                        0 );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardControl\n");

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>