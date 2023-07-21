---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsMajor
title: ISCTE_EAS::GetDetailsMajor (atscpsipparser.h)
description: The GetDetailsMajor method returns the major channel number for the details channel.
helpviewer_keywords: ["GetDetailsMajor","GetDetailsMajor method [Microsoft TV Technologies]","GetDetailsMajor method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetDetailsMajor method","ISCTE_EAS.GetDetailsMajor","ISCTE_EAS::GetDetailsMajor","ISCTE_EASGetDetailsMajor","atscpsipparser/ISCTE_EAS::GetDetailsMajor","mstv.iscte_eas_getdetailsmajor"]
old-location: mstv\iscte_eas_getdetailsmajor.htm
tech.root: mstv
ms.assetid: ecb6f06d-ccf5-44f3-ba36-b24176c3a20e
ms.date: 12/05/2018
ms.keywords: GetDetailsMajor, GetDetailsMajor method [Microsoft TV Technologies], GetDetailsMajor method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsMajor method, ISCTE_EAS.GetDetailsMajor, ISCTE_EAS::GetDetailsMajor, ISCTE_EASGetDetailsMajor, atscpsipparser/ISCTE_EAS::GetDetailsMajor, mstv.iscte_eas_getdetailsmajor
req.header: atscpsipparser.h
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
 - ISCTE_EAS::GetDetailsMajor
 - atscpsipparser/ISCTE_EAS::GetDetailsMajor
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
 - ISCTE_EAS.GetDetailsMajor
---

# ISCTE_EAS::GetDetailsMajor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetDetailsMajor</b> method returns the major channel number for the details channel.

## -parameters

### -param pwVal [out]

Receives the details_major_channel_number field.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">ISCTE_EAS::Initialize</a> method was not called.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>