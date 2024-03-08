---
UID: NF:encdec.IDTFilter3.GetProtectionType
title: IDTFilter3::GetProtectionType (encdec.h)
description: The GetProtectionType method retrieves the type of content protection that is currently in effect.
helpviewer_keywords: ["GetProtectionType","GetProtectionType method [Microsoft TV Technologies]","GetProtectionType method [Microsoft TV Technologies]","IDTFilter3 interface","IDTFilter3 interface [Microsoft TV Technologies]","GetProtectionType method","IDTFilter3.GetProtectionType","IDTFilter3::GetProtectionType","IDTFilter3GetProtectionType","encdec/IDTFilter3::GetProtectionType","mstv.idtfilter3_getprotectiontype"]
old-location: mstv\idtfilter3_getprotectiontype.htm
tech.root: mstv
ms.assetid: 6b1e4186-de85-4de8-b309-82644c8b1269
ms.date: 12/05/2018
ms.keywords: GetProtectionType, GetProtectionType method [Microsoft TV Technologies], GetProtectionType method [Microsoft TV Technologies],IDTFilter3 interface, IDTFilter3 interface [Microsoft TV Technologies],GetProtectionType method, IDTFilter3.GetProtectionType, IDTFilter3::GetProtectionType, IDTFilter3GetProtectionType, encdec/IDTFilter3::GetProtectionType, mstv.idtfilter3_getprotectiontype
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDTFilter3::GetProtectionType
 - encdec/IDTFilter3::GetProtectionType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - encdec.h
api_name:
 - IDTFilter3.GetProtectionType
---

# IDTFilter3::GetProtectionType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetProtectionType</b> method retrieves the type of content protection that is currently in effect.

## -parameters

### -param pProtectionType [out]

Receives the current protection type, specified as a member of the <a href="/previous-versions/windows/desktop/api/encdec/ne-encdec-prottype">ProtType</a> enumeration type.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter3">IDTFilter3 Interface</a>