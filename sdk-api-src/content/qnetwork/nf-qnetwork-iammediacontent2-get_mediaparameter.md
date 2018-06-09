---
UID: NF:qnetwork.IAMMediaContent2.get_MediaParameter
title: IAMMediaContent2::get_MediaParameter
author: windows-sdk-content
description: The get_MediaParameter method retrieves the value of a custom parameter in the ASX file.
old-location: dshow\iammediacontent2_get_mediaparameter.htm
old-project: DirectShow
ms.assetid: 87e018bb-2073-46df-860a-c4de99a88189
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IAMMediaContent2 interface [DirectShow],get_MediaParameter method, IAMMediaContent2.get_MediaParameter, IAMMediaContent2::get_MediaParameter, IAMMediaContent2get_MediaParameter, dshow.iammediacontent2_get_mediaparameter, get_MediaParameter, get_MediaParameter method [DirectShow], get_MediaParameter method [DirectShow],IAMMediaContent2 interface, qnetwork/IAMMediaContent2::get_MediaParameter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent2.get_MediaParameter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMMediaContent2::get_MediaParameter


## -description



The <code>get_MediaParameter</code> method retrieves the value of a custom parameter in the ASX file.



This interface is not supported.


## -parameters




### -param EntryNum

Specifies the location of the parameter in the ASX file.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
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
 


### -param bstrName

Specifies the name of the parameter.


### -param pbstrValue

Pointer to a variable that receives the value of the parameter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The caller must release the <b>BSTR</b> returned in <i>pbstrValue</i>, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/cf8381f2-2ef0-4169-8029-bce36bf3d6a9">IAMMediaContent2 Interface</a>
 

 

