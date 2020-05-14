---
UID: NF:wmsdkvalidate.WMCheckURLExtension
title: WMCheckURLExtension function (wmsdkvalidate.h)
description: The WMCheckURLExtension function examines the file name extension in the URL or file name that is passed in as an argument.helpviewer_keywords: ["WMCheckURLExtension","WMCheckURLExtension function [windows Media Format]","wmformat.wmcheckurlextension","wmsdkvalidate/WMCheckURLExtension"]
old-location: wmformat\wmcheckurlextension.htm
tech.root: wmformat
ms.assetid: f001d9e7-ccbd-4dc9-bb4b-fe45cb47700c
ms.date: 12/05/2018
ms.keywords: WMCheckURLExtension, WMCheckURLExtension function [windows Media Format], wmformat.wmcheckurlextension, wmsdkvalidate/WMCheckURLExtension
f1_keywords:
- wmsdkvalidate/WMCheckURLExtension
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
- WMCheckURLExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCheckURLExtension function


## -description



The <b>WMCheckURLExtension</b> function examines the file name extension in the URL or file name that is passed in as an argument. The extension is compared to a list of supported file types in an attempt to determine whether the file can be opened by the objects of this SDK.



If you are writing an application that can handle many different file types, you can use this function to try to quickly determine whether the file can be read using objects of the Windows Media Format SDK.


## -parameters




### -param pwszURL [in]

A wide-character <b>null</b>-terminated string containing a file name or URL.


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
The function succeeded, and the file extension is supported. This result does not indicate verification of the contents of the file, just the extension.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The URL passed is not of a type supported by the objects of the Windows Media Format SDK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszURL</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This function cannot report with absolute certainty whether a particular URL can be handled, as this cannot be determined until the URL is opened.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>
 

 

