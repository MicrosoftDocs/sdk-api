---
UID: NF:wmsdkvalidate.WMCheckURLScheme
title: WMCheckURLScheme function (wmsdkvalidate.h)
description: The WMCheckURLScheme function examines a network protocol and compares it to an internal list of supported schemes.helpviewer_keywords: ["WMCheckURLScheme","WMCheckURLScheme function [windows Media Format]","wmformat.wmcheckurlscheme","wmsdkvalidate/WMCheckURLScheme"]
old-location: wmformat\wmcheckurlscheme.htm
tech.root: wmformat
ms.assetid: b62c8cd1-0b70-4cae-8e9e-bad6634f2dfa
ms.date: 12/05/2018
ms.keywords: WMCheckURLScheme, WMCheckURLScheme function [windows Media Format], wmformat.wmcheckurlscheme, wmsdkvalidate/WMCheckURLScheme
f1_keywords:
- wmsdkvalidate/WMCheckURLScheme
dev_langs:
- c++
req.header: wmsdkvalidate.h
req.include-header: Wmsdkidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wmvcore.dll
api_name:
- WMCheckURLScheme
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCheckURLScheme function


## -description



The <b>WMCheckURLScheme</b> function examines a network protocol and compares it to an internal list of supported schemes. If you are writing an application that can handle many different network protocols, you can use this function to ascertain quickly whether a network address can be handled using the methods of the Windows Media Format SDK.




## -parameters




### -param pwszURLScheme [in]

A wide-character null-terminated string containing a network protocol designation, such as "http".


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The URL passed does not conform to any of the commonly used schemes.

</td>
</tr>
</table>
 




## -remarks



This function cannot report with absolute certainty whether a particular URL can be handled, as this cannot be determined until the URL is opened.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>
 

 

