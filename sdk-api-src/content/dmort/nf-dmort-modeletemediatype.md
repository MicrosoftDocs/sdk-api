---
UID: NF:dmort.MoDeleteMediaType
title: MoDeleteMediaType function
author: windows-sdk-content
description: The MoDeleteMediaType function deletes a media type structure that was previously allocated.
old-location: dshow\modeletemediatype.htm
old-project: DirectShow
ms.assetid: adbfe1e1-e956-48de-9ed1-9f8f4c66ff1c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MoDeleteMediaType, MoDeleteMediaType function [DirectShow], dmort/MoDeleteMediaType, dshow.modeletemediatype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dmort.h
req.include-header: Dmo.h
req.target-type: Windows
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
tech.root: 
req.typenames: DMO_PARTIAL_MEDIATYPE, *PDMO_PARTIAL_MEDIATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - MoDeleteMediaType
product: Windows
targetos: Windows
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
---

# MoDeleteMediaType function


## -description


The <b>MoDeleteMediaType</b> function deletes a media type structure that was previously allocated.


## -parameters




### -param pmt

Pointer to an initialized <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



Call this function to free a <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure that was allocated with the <a href="https://msdn.microsoft.com/f67b04b5-163e-4793-8df0-10a4b2be5025">MoCreateMediaType</a> function.

Internally, this function calls <a href="https://msdn.microsoft.com/a1f0949d-a590-4759-87b5-f47307bc3ec0">MoFreeMediaType</a> to free the format block.




