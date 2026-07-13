---
UID: NF:mpeg2data.ISectionList.GetProgramIdentifier
title: ISectionList::GetProgramIdentifier (mpeg2data.h)
description: The GetProgramIdentifier method retrieves the program identifier (PID) of the packets that this object is receiving.
helpviewer_keywords: ["GetProgramIdentifier","GetProgramIdentifier method [Microsoft TV Technologies]","GetProgramIdentifier method [Microsoft TV Technologies]","ISectionList interface","ISectionList interface [Microsoft TV Technologies]","GetProgramIdentifier method","ISectionList.GetProgramIdentifier","ISectionList::GetProgramIdentifier","ISectionListGetProgramIdentifier","mpeg2data/ISectionList::GetProgramIdentifier","mstv.isectionlist_getprogramidentifier"]
old-location: mstv\isectionlist_getprogramidentifier.htm
tech.root: mstv
ms.assetid: 25a4bd3c-ef02-4685-8c83-06025ce4410c
ms.date: 12/05/2018
ms.keywords: GetProgramIdentifier, GetProgramIdentifier method [Microsoft TV Technologies], GetProgramIdentifier method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetProgramIdentifier method, ISectionList.GetProgramIdentifier, ISectionList::GetProgramIdentifier, ISectionListGetProgramIdentifier, mpeg2data/ISectionList::GetProgramIdentifier, mstv.isectionlist_getprogramidentifier
req.header: mpeg2data.h
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
 - ISectionList::GetProgramIdentifier
 - mpeg2data/ISectionList::GetProgramIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.GetProgramIdentifier
---

# ISectionList::GetProgramIdentifier


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetProgramIdentifier</b> method retrieves the program identifier (PID) of the packets that this object is receiving.

## -parameters

### -param pPid

Receives the PID.

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

## -remarks

The PID value is set when the object is first initialized.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList Interface</a>