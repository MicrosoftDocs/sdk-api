---
UID: NF:atscpsipparser.ISCTE_EAS.GetEASEventCode
title: ISCTE_EAS::GetEASEventCode (atscpsipparser.h)
description: The GetEASEventCode method returns the EAS event code.
helpviewer_keywords: ["GetEASEventCode","GetEASEventCode method [Microsoft TV Technologies]","GetEASEventCode method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetEASEventCode method","ISCTE_EAS.GetEASEventCode","ISCTE_EAS::GetEASEventCode","ISCTE_EASGetEASEventCode","atscpsipparser/ISCTE_EAS::GetEASEventCode","mstv.iscte_eas_geteaseventcode"]
old-location: mstv\iscte_eas_geteaseventcode.htm
tech.root: mstv
ms.assetid: 9618fb6f-61f3-44cf-9605-b47a6a1e9be6
ms.date: 12/05/2018
ms.keywords: GetEASEventCode, GetEASEventCode method [Microsoft TV Technologies], GetEASEventCode method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetEASEventCode method, ISCTE_EAS.GetEASEventCode, ISCTE_EAS::GetEASEventCode, ISCTE_EASGetEASEventCode, atscpsipparser/ISCTE_EAS::GetEASEventCode, mstv.iscte_eas_geteaseventcode
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
 - ISCTE_EAS::GetEASEventCode
 - atscpsipparser/ISCTE_EAS::GetEASEventCode
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
 - ISCTE_EAS.GetEASEventCode
---

# ISCTE_EAS::GetEASEventCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetEASEventCode</b> method returns the EAS event code.

## -parameters

### -param pbVal [out]

A pointer to a buffer that receives the EAS_event_code field. The caller must allocate the buffer, which must be large enough to hold the event code. To get the required size of the buffer, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventcodelen">ISCTE_EAS::GetEASEventCodeLen</a>. The event code consists of ASCII characters.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-geteaseventcodelen">GetEASEventCodeLen</a>



<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>