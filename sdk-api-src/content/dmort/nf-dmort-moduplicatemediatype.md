---
UID: NF:dmort.MoDuplicateMediaType
title: MoDuplicateMediaType function
author: windows-sdk-content
description: The MoDuplicateMediaType function duplicates a media type structure.
old-location: dshow\moduplicatemediatype.htm
tech.root: DirectShow
ms.assetid: 8804ec3f-98c7-4305-a02c-67f5e560b4f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MoDuplicateMediaType, MoDuplicateMediaType function [DirectShow], dmort/MoDuplicateMediaType, dshow.moduplicatemediatype
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - MoDuplicateMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MoDuplicateMediaType function


## -description


The <b>MoDuplicateMediaType</b> function duplicates a media type structure.


## -parameters




### -param ppmtDest

Address of a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd375504(v=VS.85).aspx">DMO_MEDIA_TYPE</a> structure that receives the duplicated structure.


### -param pmtSrc

Pointer to the media type structure to duplicate.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
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



This method is equivalent to calling <a href="https://msdn.microsoft.com/en-us/library/Dd390694(v=VS.85).aspx">MoCreateMediaType</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd390693(v=VS.85).aspx">MoCopyMediaType</a>. The caller must delete the returned media type structure by calling the <a href="https://msdn.microsoft.com/en-us/library/Dd390695(v=VS.85).aspx">MoDeleteMediaType</a> function.



