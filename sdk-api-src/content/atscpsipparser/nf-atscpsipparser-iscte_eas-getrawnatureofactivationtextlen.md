---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawNatureOfActivationTextLen
title: ISCTE_EAS::GetRawNatureOfActivationTextLen (atscpsipparser.h)
description: Gets the length of the nature_of_activation_text field.
helpviewer_keywords: ["GetRawNatureOfActivationTextLen","GetRawNatureOfActivationTextLen method [Microsoft TV Technologies]","GetRawNatureOfActivationTextLen method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetRawNatureOfActivationTextLen method","ISCTE_EAS.GetRawNatureOfActivationTextLen","ISCTE_EAS::GetRawNatureOfActivationTextLen","atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationTextLen","mstv.iscte_eas_getrawnatureofactivationtextlen"]
old-location: mstv\iscte_eas_getrawnatureofactivationtextlen.htm
tech.root: mstv
ms.assetid: a7f93884-d8a9-449b-afc2-b2ccbd0d2492
ms.date: 12/05/2018
ms.keywords: GetRawNatureOfActivationTextLen, GetRawNatureOfActivationTextLen method [Microsoft TV Technologies], GetRawNatureOfActivationTextLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawNatureOfActivationTextLen method, ISCTE_EAS.GetRawNatureOfActivationTextLen, ISCTE_EAS::GetRawNatureOfActivationTextLen, atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationTextLen, mstv.iscte_eas_getrawnatureofactivationtextlen
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
 - ISCTE_EAS::GetRawNatureOfActivationTextLen
 - atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationTextLen
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
 - ISCTE_EAS.GetRawNatureOfActivationTextLen
---

# ISCTE_EAS::GetRawNatureOfActivationTextLen


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of the nature_of_activation_text field.

## -parameters

### -param pbVal [out]

Receives the size of the nature_of_activation_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawnatureofactivationtext">ISCTE_EAS::GetRawNatureOfActivationText</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a>



<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getnatureofactivationtext">ISCTE_EAS::GetNatureOfActivationText</a>