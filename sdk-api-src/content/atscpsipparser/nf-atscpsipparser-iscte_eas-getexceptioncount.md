---
UID: NF:atscpsipparser.ISCTE_EAS.GetExceptionCount
title: ISCTE_EAS::GetExceptionCount (atscpsipparser.h)
description: The GetExceptionCount method returns the number of exception services.
helpviewer_keywords: ["GetExceptionCount","GetExceptionCount method [Microsoft TV Technologies]","GetExceptionCount method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetExceptionCount method","ISCTE_EAS.GetExceptionCount","ISCTE_EAS::GetExceptionCount","ISCTE_EASGetExceptionCount","atscpsipparser/ISCTE_EAS::GetExceptionCount","mstv.iscte_eas_getexceptioncount"]
old-location: mstv\iscte_eas_getexceptioncount.htm
tech.root: mstv
ms.assetid: da98cf2f-a302-41d0-8226-18d6bb89be82
ms.date: 12/05/2018
ms.keywords: GetExceptionCount, GetExceptionCount method [Microsoft TV Technologies], GetExceptionCount method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetExceptionCount method, ISCTE_EAS.GetExceptionCount, ISCTE_EAS::GetExceptionCount, ISCTE_EASGetExceptionCount, atscpsipparser/ISCTE_EAS::GetExceptionCount, mstv.iscte_eas_getexceptioncount
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
 - ISCTE_EAS::GetExceptionCount
 - atscpsipparser/ISCTE_EAS::GetExceptionCount
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
 - ISCTE_EAS.GetExceptionCount
---

# ISCTE_EAS::GetExceptionCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetExceptionCount</b> method returns the number of exception services.

## -parameters

### -param pbVal [out]

Receives the exception_count field.

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