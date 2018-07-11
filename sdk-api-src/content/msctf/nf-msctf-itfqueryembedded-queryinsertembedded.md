---
UID: NF:msctf.ITfQueryEmbedded.QueryInsertEmbedded
title: ITfQueryEmbedded::QueryInsertEmbedded
author: windows-sdk-content
description: ITfQueryEmbedded::QueryInsertEmbedded method
old-location: tsf\itfqueryembedded_queryinsertembedded.htm
old-project: TSF
ms.assetid: 52f9465f-725e-493b-89ee-1b3db3cef696
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfQueryEmbedded interface [Text Services Framework],QueryInsertEmbedded method, ITfQueryEmbedded.QueryInsertEmbedded, ITfQueryEmbedded::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITfQueryEmbedded interface, _tsf_itfqueryembedded_queryinsertembedded_ref, msctf/ITfQueryEmbedded::QueryInsertEmbedded, tsf.itfqueryembedded_queryinsertembedded
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfQueryEmbedded.QueryInsertEmbedded
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfQueryEmbedded::QueryInsertEmbedded


## -description




## -parameters




### -param pguidService [in]

A GUID that identifies the service associated with the object. This value can be <b>NULL</b> if <i>pFormatEtc</i> is valid.


### -param pFormatEtc [in]

Pointer to a <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that contains data about the object to be embedded. This value can be <b>NULL</b> if <i>pguidService</i> is valid.


### -param pfInsertable [out]

Pointer to a Boolean value that receives the query result. This value receives a nonzero value if the object can be embedded, or zero otherwise.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
There is no active context.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6e2c3ad5-73c6-481f-9ade-58782e12dfbd">ITfQueryEmbedded</a>



<a href="https://msdn.microsoft.com/46d8988a-4b97-4c86-8b1b-db87044a7e01">The FORMATETC Structure</a>
 

 

