---
UID: NF:mpeg2psiparser.IPMT.GetCountOfTableDescriptors
title: IPMT::GetCountOfTableDescriptors (mpeg2psiparser.h)
description: The GetCountOfTableDescriptors method returns the number of table-wide descriptors in the PMT.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IPMT interface","IPMT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IPMT.GetCountOfTableDescriptors","IPMT::GetCountOfTableDescriptors","IPMTGetCountOfTableDescriptors","mpeg2psiparser/IPMT::GetCountOfTableDescriptors","mstv.ipmt_getcountoftabledescriptors"]
old-location: mstv\ipmt_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: e1f91a13-afec-4703-8f1c-be64c8a8b8f9
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IPMT.GetCountOfTableDescriptors, IPMT::GetCountOfTableDescriptors, IPMTGetCountOfTableDescriptors, mpeg2psiparser/IPMT::GetCountOfTableDescriptors, mstv.ipmt_getcountoftabledescriptors
f1_keywords:
- mpeg2psiparser/IPMT.GetCountOfTableDescriptors
dev_langs:
- c++
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
- IPMT.GetCountOfTableDescriptors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>
 

 

