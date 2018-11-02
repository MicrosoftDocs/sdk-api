---
UID: NF:qnetwork.IAMMediaContent2.get_MediaParameterName
title: IAMMediaContent2::get_MediaParameterName
author: windows-sdk-content
description: The get_MediaParameterName method retrieves the name of a custom parameter in an ASX file.
old-location: dshow\iammediacontent2_get_mediaparametername.htm
tech.root: DirectShow
ms.assetid: 67eb8a01-312a-45ee-8da3-59a1f9f952ec
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAMMediaContent2 interface [DirectShow],get_MediaParameterName method, IAMMediaContent2.get_MediaParameterName, IAMMediaContent2::get_MediaParameterName, IAMMediaContent2get_MediaParameterName, dshow.iammediacontent2_get_mediaparametername, get_MediaParameterName, get_MediaParameterName method [DirectShow], get_MediaParameterName method [DirectShow],IAMMediaContent2 interface, qnetwork/IAMMediaContent2::get_MediaParameterName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent2.get_MediaParameterName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaContent2::get_MediaParameterName


## -description



The <code>get_MediaParameterName</code> method retrieves the name of a custom parameter in an ASX file.



This interface is not supported.


## -parameters




### -param EntryNum

Specifies the location of the parameter in the ASX file.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The parameter is a direct child of the ASX node.</td>
</tr>
<tr>
<td>&gt; 0</td>
<td>The parameter is located inside an ENTRY tag; <i>EntryNum</i> specifies the entry, indexed from 1.</td>
</tr>
</table>
 


### -param Index

Specifies the index of the parameter to retrieve, indexed from 1.


### -param pbstrName

Pointer to a variable that receives the parameter name.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/cf8381f2-2ef0-4169-8029-bce36bf3d6a9">IAMMediaContent2 Interface</a>
 

 

