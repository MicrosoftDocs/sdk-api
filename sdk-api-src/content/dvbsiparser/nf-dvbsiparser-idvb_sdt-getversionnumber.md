---
UID: NF:dvbsiparser.IDVB_SDT.GetVersionNumber
title: IDVB_SDT::GetVersionNumber (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IDVB_SDT interface","IDVB_SDT interface [Microsoft TV Technologies]","GetVersionNumber method","IDVB_SDT.GetVersionNumber","IDVB_SDT::GetVersionNumber","IDVB_SDTGetVersionNumber","dvbsiparser/IDVB_SDT::GetVersionNumber","mstv.idvb_sdt_getversionnumber"]
old-location: mstv\idvb_sdt_getversionnumber.htm
tech.root: mstv
ms.assetid: ea39c890-86d5-4eef-8c50-3edfd0d1ec8d
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetVersionNumber method, IDVB_SDT.GetVersionNumber, IDVB_SDT::GetVersionNumber, IDVB_SDTGetVersionNumber, dvbsiparser/IDVB_SDT::GetVersionNumber, mstv.idvb_sdt_getversionnumber
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
 - IDVB_SDT::GetVersionNumber
 - dvbsiparser/IDVB_SDT::GetVersionNumber
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
 - IDVB_SDT.GetVersionNumber
---

# IDVB_SDT::GetVersionNumber


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionNumber</b> method returns the version number for the SDT.

## -parameters

### -param pbVal [out]

Pointer to a variable that receives the version_number field.

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

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_sdt">IDVB_SDT Interface</a>