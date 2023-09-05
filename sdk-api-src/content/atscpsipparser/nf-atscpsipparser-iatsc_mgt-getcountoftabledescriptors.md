---
UID: NF:atscpsipparser.IATSC_MGT.GetCountOfTableDescriptors
title: IATSC_MGT::GetCountOfTableDescriptors (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IATSC_MGT interface","IATSC_MGT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IATSC_MGT.GetCountOfTableDescriptors","IATSC_MGT::GetCountOfTableDescriptors","IATSC_MGTGetCountOfTableDescriptors","atscpsipparser/IATSC_MGT::GetCountOfTableDescriptors","mstv.iatsc_mgt_getcountoftabledescriptors"]
old-location: mstv\iatsc_mgt_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 14bd596f-ca24-456b-bb53-4e7e37183422
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IATSC_MGT interface, IATSC_MGT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IATSC_MGT.GetCountOfTableDescriptors, IATSC_MGT::GetCountOfTableDescriptors, IATSC_MGTGetCountOfTableDescriptors, atscpsipparser/IATSC_MGT::GetCountOfTableDescriptors, mstv.iatsc_mgt_getcountoftabledescriptors
req.header: atscpsipparser.h
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
 - IATSC_MGT::GetCountOfTableDescriptors
 - atscpsipparser/IATSC_MGT::GetCountOfTableDescriptors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_MGT.GetCountOfTableDescriptors
---

# IATSC_MGT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the MGT.

## -parameters

### -param pdwVal [in]

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_mgt">IATSC_MGT Interface</a>