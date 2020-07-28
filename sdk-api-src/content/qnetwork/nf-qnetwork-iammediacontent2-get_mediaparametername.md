---
UID: NF:qnetwork.IAMMediaContent2.get_MediaParameterName
title: IAMMediaContent2::get_MediaParameterName (qnetwork.h)
description: The get_MediaParameterName method retrieves the name of a custom parameter in an ASX file.
helpviewer_keywords: ["IAMMediaContent2 interface [DirectShow]","get_MediaParameterName method","IAMMediaContent2.get_MediaParameterName","IAMMediaContent2::get_MediaParameterName","IAMMediaContent2get_MediaParameterName","dshow.iammediacontent2_get_mediaparametername","get_MediaParameterName","get_MediaParameterName method [DirectShow]","get_MediaParameterName method [DirectShow]","IAMMediaContent2 interface","qnetwork/IAMMediaContent2::get_MediaParameterName"]
old-location: dshow\iammediacontent2_get_mediaparametername.htm
tech.root: dshow
ms.assetid: 67eb8a01-312a-45ee-8da3-59a1f9f952ec
ms.date: 12/05/2018
ms.keywords: IAMMediaContent2 interface [DirectShow],get_MediaParameterName method, IAMMediaContent2.get_MediaParameterName, IAMMediaContent2::get_MediaParameterName, IAMMediaContent2get_MediaParameterName, dshow.iammediacontent2_get_mediaparametername, get_MediaParameterName, get_MediaParameterName method [DirectShow], get_MediaParameterName method [DirectShow],IAMMediaContent2 interface, qnetwork/IAMMediaContent2::get_MediaParameterName
f1_keywords:
- qnetwork/IAMMediaContent2.get_MediaParameterName
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent2">IAMMediaContent2 Interface</a>
 

 

