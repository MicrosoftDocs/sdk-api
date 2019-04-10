---
UID: NF:mpeg2psiparser.IGenericDescriptor.GetBody
title: IGenericDescriptor::GetBody (mpeg2psiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\igenericdescriptor_getbody.htm
tech.root: mstv
ms.assetid: fbb17e16-b0a4-45c1-b723-cbb6a61d4d0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBody, GetBody method [Microsoft TV Technologies], GetBody method [Microsoft TV Technologies],IGenericDescriptor interface, IGenericDescriptor interface [Microsoft TV Technologies],GetBody method, IGenericDescriptor.GetBody, IGenericDescriptor::GetBody, IGenericDescriptorGetBody, mpeg2psiparser/IGenericDescriptor::GetBody, mstv.igenericdescriptor_getbody
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IGenericDescriptor.GetBody
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGenericDescriptor::GetBody


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetBody</b> method returns the body of the descriptor.


## -parameters




### -param ppbVal [out]

Receives a pointer to a buffer. To get the size of the buffer, call the <a href="https://msdn.microsoft.com/en-us/library/Dd694095(v=VS.85).aspx">IGenericDescriptor::GetLength</a> method. The buffer contains the body of the descriptor, in network byte order (Big Endian). The caller is responsible for converting the data to Little Endian byte order. The caller must free the buffer by calling the <b>CoTaskMemFree</b> function.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694093(v=VS.85).aspx">IGenericDescriptor Interface</a>
 

 

