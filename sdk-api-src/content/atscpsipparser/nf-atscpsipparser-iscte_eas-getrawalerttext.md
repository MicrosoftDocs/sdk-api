---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawAlertText
title: ISCTE_EAS::GetRawAlertText (atscpsipparser.h)
description: Gets the raw alert_text field from the EAS table.
helpviewer_keywords: ["GetRawAlertText","GetRawAlertText method [Microsoft TV Technologies]","GetRawAlertText method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetRawAlertText method","ISCTE_EAS.GetRawAlertText","ISCTE_EAS::GetRawAlertText","atscpsipparser/ISCTE_EAS::GetRawAlertText","mstv.iscte_eas_getrawalerttext"]
old-location: mstv\iscte_eas_getrawalerttext.htm
tech.root: mstv
ms.assetid: e5ed18e8-e83e-4708-995b-99acd12427a7
ms.date: 12/05/2018
ms.keywords: GetRawAlertText, GetRawAlertText method [Microsoft TV Technologies], GetRawAlertText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawAlertText method, ISCTE_EAS.GetRawAlertText, ISCTE_EAS::GetRawAlertText, atscpsipparser/ISCTE_EAS::GetRawAlertText, mstv.iscte_eas_getrawalerttext
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
 - ISCTE_EAS::GetRawAlertText
 - atscpsipparser/ISCTE_EAS::GetRawAlertText
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
 - ISCTE_EAS.GetRawAlertText
---

# ISCTE_EAS::GetRawAlertText


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the raw alert_text field from the EAS table.

## -parameters

### -param pbVal [out]

A pointer to a buffer that receives the alert_text field. The caller must allocate the buffer. To get the required size of the buffer, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawalerttextlen">ISCTE_EAS::GetRawAlertTextLen</a>. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the alert text for a specific language, call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getalerttext">ISCTE_EAS::GetAlertText</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a>



<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getalerttext">ISCTE_EAS::GetAlertText</a>