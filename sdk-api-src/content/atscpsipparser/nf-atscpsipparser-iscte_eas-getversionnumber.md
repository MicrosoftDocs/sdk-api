---
UID: NF:atscpsipparser.ISCTE_EAS.GetVersionNumber
title: ISCTE_EAS::GetVersionNumber (atscpsipparser.h)
description: The GetVersionNumber method returns the version number for the EAS table.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetVersionNumber method","ISCTE_EAS.GetVersionNumber","ISCTE_EAS::GetVersionNumber","ISCTE_EASGetVersionNumber","atscpsipparser/ISCTE_EAS::GetVersionNumber","mstv.iscte_eas_getversionnumber"]
old-location: mstv\iscte_eas_getversionnumber.htm
tech.root: mstv
ms.assetid: b2108435-37ef-404c-b735-a5100acfa8a4
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetVersionNumber method, ISCTE_EAS.GetVersionNumber, ISCTE_EAS::GetVersionNumber, ISCTE_EASGetVersionNumber, atscpsipparser/ISCTE_EAS::GetVersionNumber, mstv.iscte_eas_getversionnumber
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
 - ISCTE_EAS::GetVersionNumber
 - atscpsipparser/ISCTE_EAS::GetVersionNumber
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
 - ISCTE_EAS.GetVersionNumber
---

# ISCTE_EAS::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetVersionNumber</b> method returns the version number for the EAS table.

## -parameters

### -param pbVal [out]

Receives the version_number field.

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