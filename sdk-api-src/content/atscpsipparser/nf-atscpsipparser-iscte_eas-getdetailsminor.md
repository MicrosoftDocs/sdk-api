---
UID: NF:atscpsipparser.ISCTE_EAS.GetDetailsMinor
title: ISCTE_EAS::GetDetailsMinor (atscpsipparser.h)
description: The GetDetailsMinor method returns the minor channel number for the details channel.
helpviewer_keywords: ["GetDetailsMinor","GetDetailsMinor method [Microsoft TV Technologies]","GetDetailsMinor method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetDetailsMinor method","ISCTE_EAS.GetDetailsMinor","ISCTE_EAS::GetDetailsMinor","ISCTE_EASGetDetailsMinor","atscpsipparser/ISCTE_EAS::GetDetailsMinor","mstv.iscte_eas_getdetailsminor"]
old-location: mstv\iscte_eas_getdetailsminor.htm
tech.root: mstv
ms.assetid: 59d43d84-2120-4200-b1e7-4603c1693018
ms.date: 12/05/2018
ms.keywords: GetDetailsMinor, GetDetailsMinor method [Microsoft TV Technologies], GetDetailsMinor method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetDetailsMinor method, ISCTE_EAS.GetDetailsMinor, ISCTE_EAS::GetDetailsMinor, ISCTE_EASGetDetailsMinor, atscpsipparser/ISCTE_EAS::GetDetailsMinor, mstv.iscte_eas_getdetailsminor
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
 - ISCTE_EAS::GetDetailsMinor
 - atscpsipparser/ISCTE_EAS::GetDetailsMinor
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
 - ISCTE_EAS.GetDetailsMinor
---

# ISCTE_EAS::GetDetailsMinor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetDetailsMinor</b> method returns the minor channel number for the details channel.

## -parameters

### -param pwVal [out]

Receives the details_minor_channel_number field.

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