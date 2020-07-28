---
UID: NF:mpeg2psiparser.ITSDT.GetCountOfTableDescriptors
title: ITSDT::GetCountOfTableDescriptors (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","ITSDT interface","ITSDT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","ITSDT.GetCountOfTableDescriptors","ITSDT::GetCountOfTableDescriptors","ITSDTGetCountOfTableDescriptors","mpeg2psiparser/ITSDT::GetCountOfTableDescriptors","mstv.itsdt_getcountoftabledescriptors"]
old-location: mstv\itsdt_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 29e2f3f7-4ff4-447b-bd17-36cd05829844
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, ITSDT.GetCountOfTableDescriptors, ITSDT::GetCountOfTableDescriptors, ITSDTGetCountOfTableDescriptors, mpeg2psiparser/ITSDT::GetCountOfTableDescriptors, mstv.itsdt_getcountoftabledescriptors
f1_keywords:
- mpeg2psiparser/ITSDT.GetCountOfTableDescriptors
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
- ITSDT.GetCountOfTableDescriptors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSDT::GetCountOfTableDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the TSDT.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-itsdt">ITSDT Interface</a>
 

 

