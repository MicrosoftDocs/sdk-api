---
UID: NF:wsdutil.WSDUriEncode
title: WSDUriEncode function
author: windows-driver-content
description: Encodes a URI according to URI encoding rules in RFC2396.
old-location: ncd\wsduriencode.htm
old-project: WsdApi
ms.assetid: 3d086ac8-0c14-46fb-baa5-b1d89b86ebbb
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSDUriEncode, WSDUriEncode function, ncd.wsduriencode, wsdutil/WSDUriEncode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsdapi.dll
api_name:
-	WSDUriEncode
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDUriEncode function


## -description


Encodes a URI according to URI encoding rules in RFC2396.


## -parameters




### -param source [in]

Contains the URI to be encoded.


### -param cchSource [in]

Specifies the length of <i>source</i> in characters.


### -param destOut [out]

Pointer to a string that contains the encoded URI.  If <i>destOut</i> is not <b>NULL</b>, the calling application should free the allocated string by calling <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.


### -param cchDestOut [out, optional]

Specifies the length of <i>destOut</i> in characters.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>source</i> is <b>NULL</b> or <i>cchSource</i> is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>source</i> exceeds <b>WSD_MAX_TEXT_LENGTH</b> (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>destOut</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>WSDUriEncode</b> encodes certain characters in <i>source</i> into an escaped encoding format of %XY, where X and Y are hexadecimal digits corresponding to the single-byte representation of that character.  Wide characters that occupy multiple bytes are first rendered into UTF-8 multi-byte format, and then escaped into encoded characters.

<b>WSDUriEncode</b> does not encode single-byte alphanumeric characters.  It does encode percent signs (%) in <i>source</i>.



