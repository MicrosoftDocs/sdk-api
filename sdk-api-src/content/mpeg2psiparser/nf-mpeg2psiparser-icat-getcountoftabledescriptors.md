---
UID: NF:mpeg2psiparser.ICAT.GetCountOfTableDescriptors
title: ICAT::GetCountOfTableDescriptors
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icat_getcountoftabledescriptors.htm
old-project: mstv
ms.assetid: 3111eecc-b869-4235-8af4-cc0ef9cc5e4e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],ICAT interface, ICAT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, ICAT.GetCountOfTableDescriptors, ICAT::GetCountOfTableDescriptors, ICATGetCountOfTableDescriptors, mpeg2psiparser/ICAT::GetCountOfTableDescriptors, mstv.icat_getcountoftabledescriptors
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mpeg2psiparser.h
api_name:
 - ICAT.GetCountOfTableDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ICAT::GetCountOfTableDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the CAT.


## -parameters




### -param pdwVal [out]

Receives the number of descriptors.


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




<a href="https://msdn.microsoft.com/00da2af8-0f1a-467a-b310-8b8c7e564013">ICAT Interface</a>
 

 

