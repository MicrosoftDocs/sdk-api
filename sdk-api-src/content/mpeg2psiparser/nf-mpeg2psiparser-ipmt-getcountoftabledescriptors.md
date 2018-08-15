---
UID: NF:mpeg2psiparser.IPMT.GetCountOfTableDescriptors
title: IPMT::GetCountOfTableDescriptors
author: windows-sdk-content
description: The GetCountOfTableDescriptors method returns the number of table-wide descriptors in the PMT.
old-location: mstv\ipmt_getcountoftabledescriptors.htm
old-project: mstv
ms.assetid: e1f91a13-afec-4703-8f1c-be64c8a8b8f9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IPMT.GetCountOfTableDescriptors, IPMT::GetCountOfTableDescriptors, IPMTGetCountOfTableDescriptors, mpeg2psiparser/IPMT::GetCountOfTableDescriptors, mstv.ipmt_getcountoftabledescriptors
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: 
req.redist: 
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
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetCountOfTableDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetCountOfTableDescriptors


## -description



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the PMT.




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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

