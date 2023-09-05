---
UID: NF:atscpsipparser.ISCTE_EAS.GetNatureOfActivationText
title: ISCTE_EAS::GetNatureOfActivationText (atscpsipparser.h)
description: The GetNatureOfActivationText method gets a textual representation of the alert for a specified ISO 639 language code.
helpviewer_keywords: ["GetNatureOfActivationText","GetNatureOfActivationText method [Microsoft TV Technologies]","GetNatureOfActivationText method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetNatureOfActivationText method","ISCTE_EAS.GetNatureOfActivationText","ISCTE_EAS::GetNatureOfActivationText","ISCTE_EASGetNatureOfActivationText","atscpsipparser/ISCTE_EAS::GetNatureOfActivationText","mstv.iscte_eas_getnatureofactivationtext"]
old-location: mstv\iscte_eas_getnatureofactivationtext.htm
tech.root: mstv
ms.assetid: 36cb57f1-b894-4c41-b555-db15f8dbe516
ms.date: 12/05/2018
ms.keywords: GetNatureOfActivationText, GetNatureOfActivationText method [Microsoft TV Technologies], GetNatureOfActivationText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetNatureOfActivationText method, ISCTE_EAS.GetNatureOfActivationText, ISCTE_EAS::GetNatureOfActivationText, ISCTE_EASGetNatureOfActivationText, atscpsipparser/ISCTE_EAS::GetNatureOfActivationText, mstv.iscte_eas_getnatureofactivationtext
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
 - ISCTE_EAS::GetNatureOfActivationText
 - atscpsipparser/ISCTE_EAS::GetNatureOfActivationText
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
 - ISCTE_EAS.GetNatureOfActivationText
---

# ISCTE_EAS::GetNatureOfActivationText


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetNatureOfActivationText</b> method gets a textual representation of the alert for a specified ISO 639 language code.

## -parameters

### -param bstrIS0639code [in]

The ISO 639 language code.

### -param pbstrString [out]

Receives the text as a <b>BSTR</b>. The caller must free the string by calling <b>SysFreeString</b>.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The specified language is not present.

</td>
</tr>
</table>

## -remarks

The returned string is taken from the nature_of_activation_text field, as defined by ANSI-J-STD-042-A.

<div class="alert"><b>Note</b>  An earlier version of the documentation gave an incorrect signature for this method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>