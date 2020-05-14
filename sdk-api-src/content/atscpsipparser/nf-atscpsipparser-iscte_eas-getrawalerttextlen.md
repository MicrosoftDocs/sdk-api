---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawAlertTextLen
title: ISCTE_EAS::GetRawAlertTextLen (atscpsipparser.h)
description: Gets the length of the alert_text field.helpviewer_keywords: ["GetRawAlertTextLen","GetRawAlertTextLen method [Microsoft TV Technologies]","GetRawAlertTextLen method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetRawAlertTextLen method","ISCTE_EAS.GetRawAlertTextLen","ISCTE_EAS::GetRawAlertTextLen","atscpsipparser/ISCTE_EAS::GetRawAlertTextLen","mstv.iscte_eas_getrawalerttextlen"]
old-location: mstv\iscte_eas_getrawalerttextlen.htm
tech.root: mstv
ms.assetid: e85b1deb-6e93-4187-8a18-80740ce9e4c9
ms.date: 12/05/2018
ms.keywords: GetRawAlertTextLen, GetRawAlertTextLen method [Microsoft TV Technologies], GetRawAlertTextLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawAlertTextLen method, ISCTE_EAS.GetRawAlertTextLen, ISCTE_EAS::GetRawAlertTextLen, atscpsipparser/ISCTE_EAS::GetRawAlertTextLen, mstv.iscte_eas_getrawalerttextlen
f1_keywords:
- atscpsipparser/ISCTE_EAS.GetRawAlertTextLen
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
- ISCTE_EAS.GetRawAlertTextLen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::GetRawAlertTextLen


## -description


Gets the length of the alert_text field.


## -parameters




### -param pwVal [out]

Receives the size of the alert_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getrawalerttext">ISCTE_EAS::GetRawAlertText</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getalerttext">ISCTE_EAS::GetAlertText</a>
 

 

