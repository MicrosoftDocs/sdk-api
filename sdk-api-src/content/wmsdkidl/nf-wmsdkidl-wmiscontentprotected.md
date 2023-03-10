---
UID: NF:wmsdkidl.WMIsContentProtected
title: WMIsContentProtected function (wmsdkidl.h)
description: The WMIsContentProtected function checks a file for DRM-protected content. This function is a shortcut so that your application can quickly identify protected files.
helpviewer_keywords: ["WMIsContentProtected","WMIsContentProtected function [windows Media Format]","wmformat.wmiscontentprotected","wmsdkidl/WMIsContentProtected"]
old-location: wmformat\wmiscontentprotected.htm
tech.root: wmformat
ms.assetid: a28cdf06-8c4f-41ff-b9dc-eddf9bc9d674
ms.date: 12/05/2018
ms.keywords: WMIsContentProtected, WMIsContentProtected function [windows Media Format], wmformat.wmiscontentprotected, wmsdkidl/WMIsContentProtected
req.header: wmsdkidl.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMIsContentProtected
 - wmsdkidl/WMIsContentProtected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMIsContentProtected
---

# WMIsContentProtected function


## -description

The <b>WMIsContentProtected</b> function checks a file for DRM-protected content. This function is a shortcut so that your application can quickly identify protected files.

## -parameters

### -param pwszFileName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the file to check for DRM-protected content.

### -param pfIsProtected [out]

Pointer to a Boolean value that is set to True on function return if the file contains DRM-protected content.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The content is unprotected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>