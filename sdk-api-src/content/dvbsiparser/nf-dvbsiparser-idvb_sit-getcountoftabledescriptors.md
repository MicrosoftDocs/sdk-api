---
UID: NF:dvbsiparser.IDVB_SIT.GetCountOfTableDescriptors
title: IDVB_SIT::GetCountOfTableDescriptors (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IDVB_SIT interface","IDVB_SIT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IDVB_SIT.GetCountOfTableDescriptors","IDVB_SIT::GetCountOfTableDescriptors","IDVB_SITGetCountOfTableDescriptors","dvbsiparser/IDVB_SIT::GetCountOfTableDescriptors","mstv.idvb_sit_getcountoftabledescriptors"]
old-location: mstv\idvb_sit_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 7fe03fe0-f12e-43cb-b340-26fffdf2d873
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IDVB_SIT interface, IDVB_SIT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IDVB_SIT.GetCountOfTableDescriptors, IDVB_SIT::GetCountOfTableDescriptors, IDVB_SITGetCountOfTableDescriptors, dvbsiparser/IDVB_SIT::GetCountOfTableDescriptors, mstv.idvb_sit_getcountoftabledescriptors
req.header: dvbsiparser.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDVB_SIT::GetCountOfTableDescriptors
 - dvbsiparser/IDVB_SIT::GetCountOfTableDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_SIT.GetCountOfTableDescriptors
---

# IDVB_SIT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the SIT.

## -parameters

### -param pdwVal [out]

Pointer to a variable that receives the number of descriptors.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sit">IDVB_SIT Interface</a>