---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

