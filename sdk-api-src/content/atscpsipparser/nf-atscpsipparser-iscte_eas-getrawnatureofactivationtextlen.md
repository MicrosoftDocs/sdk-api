---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawNatureOfActivationTextLen
title: ISCTE_EAS::GetRawNatureOfActivationTextLen (atscpsipparser.h)

description: Gets the length of the nature_of_activation_text field.
old-location: mstv\iscte_eas_getrawnatureofactivationtextlen.htm
tech.root: mstv
ms.assetid: a7f93884-d8a9-449b-afc2-b2ccbd0d2492

ms.date: 12/05/2018
ms.keywords: GetRawNatureOfActivationTextLen, GetRawNatureOfActivationTextLen method [Microsoft TV Technologies], GetRawNatureOfActivationTextLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawNatureOfActivationTextLen method, ISCTE_EAS.GetRawNatureOfActivationTextLen, ISCTE_EAS::GetRawNatureOfActivationTextLen, atscpsipparser/ISCTE_EAS::GetRawNatureOfActivationTextLen, mstv.iscte_eas_getrawnatureofactivationtextlen
ms.topic: method
f1_keywords: 
 - "atscpsipparser/ISCTE_EAS.GetRawNatureOfActivationTextLen"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ISCTE_EAS.GetRawNatureOfActivationTextLen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::GetRawNatureOfActivationTextLen


## -description


Gets the length of the nature_of_activation_text field.


## -parameters




### -param pbVal [out]

Receives the size of the nature_of_activation_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawnatureofactivationtext">ISCTE_EAS::GetRawNatureOfActivationText</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getnatureofactivationtext">ISCTE_EAS::GetNatureOfActivationText</a>
 

 

