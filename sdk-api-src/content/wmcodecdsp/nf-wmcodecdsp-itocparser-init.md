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

# ITocParser::Init


## -description


The <b>Init</b> method initializes the TOC Parser object and associates it with a media file.


## -parameters




### -param pwszFileName [in]

Pointer to a NULL-terminated wide-character string that specifies the path of the media file. See Remarks.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The path that you pass in <i>pwszFileName</i> must be a long Universal Naming Convention (UNC) file path. A long UNC file path begins with "\\?\". The following line of code shows how to set the path for the file c:\experiment\seattle.wmv.

<code>pTocParser-&gt;Init(L"\\\\?\\c:\\experiment\\seattle.wmv");</code>




## -see-also




<a href="https://msdn.microsoft.com/d1f14a6e-d75c-4266-beff-0e9af911edfe">ITocParser</a>
 

 

