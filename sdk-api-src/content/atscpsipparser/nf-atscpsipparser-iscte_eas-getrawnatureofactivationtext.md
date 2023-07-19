---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawNatureOfActivationText
title: ISCTE_EAS::GetRawNatureOfActivationText (atscpsipparser.h)
description: Gets the raw nature_of_activation_text field from the EAS table.
helpviewer_keywords: ["GetRawNatureOfActivationText","GetRawNatureOfActivationText method [Microsoft TV Technologies]","GetRawNatureOfActivationText method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetRawNatureOfActivationText method","ISCTE_EAS.GetRawNatureOfActivationText","ISCTE_EAS::GetRawNatureOfActivationText","atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationText","mstv.iscte_eas_getrawnatureofactivationtext"]
old-location: mstv\iscte_eas_getrawnatureofactivationtext.htm
tech.root: mstv
ms.assetid: 11ada9ab-b55f-41c1-9d7d-1c856a17a3a9
ms.date: 12/05/2018
ms.keywords: GetRawNatureOfActivationText, GetRawNatureOfActivationText method [Microsoft TV Technologies], GetRawNatureOfActivationText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawNatureOfActivationText method, ISCTE_EAS.GetRawNatureOfActivationText, ISCTE_EAS::GetRawNatureOfActivationText, atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationText, mstv.iscte_eas_getrawnatureofactivationtext
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
 - ISCTE_EAS::GetRawNatureOfActivationText
 - atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationText
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
 - ISCTE_EAS.GetRawNatureOfActivationText
---

# ISCTE_EAS::GetRawNatureOfActivationText


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the raw nature_of_activation_text field from the EAS table.

## -parameters

### -param pbVal [out]

A pointer to a buffer that receives the nature_of_activation_text field. The caller must allocate the buffer. To get the required size of the buffer, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawnatureofactivationtextlen">ISCTE_EAS::GetRawNatureOfActivationTextLen</a>. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the text for a specific language, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getnatureofactivationtext">ISCTE_EAS::GetNatureOfActivationText</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a>



<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getnatureofactivationtext">ISCTE_EAS::GetNatureOfActivationText</a>