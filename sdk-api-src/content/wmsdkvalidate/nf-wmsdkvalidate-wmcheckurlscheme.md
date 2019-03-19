---
UID: NF:wmsdkvalidate.WMCheckURLScheme
title: WMCheckURLScheme function (wmsdkvalidate.h)
author: windows-sdk-content
description: The WMCheckURLScheme function examines a network protocol and compares it to an internal list of supported schemes.
old-location: wmformat\wmcheckurlscheme.htm
tech.root: wmformat
ms.assetid: b62c8cd1-0b70-4cae-8e9e-bad6634f2dfa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMCheckURLScheme, WMCheckURLScheme function [windows Media Format], wmformat.wmcheckurlscheme, wmsdkvalidate/WMCheckURLScheme
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>
 

 

