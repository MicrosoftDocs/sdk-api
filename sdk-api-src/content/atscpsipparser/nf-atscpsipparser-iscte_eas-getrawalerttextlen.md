---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawAlertTextLen
title: ISCTE_EAS::GetRawAlertTextLen
author: windows-driver-content
description: Gets the length of the alert_text field.
old-location: mstv\iscte_eas_getrawalerttextlen.htm
old-project: mstv
ms.assetid: e85b1deb-6e93-4187-8a18-80740ce9e4c9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRawAlertTextLen, GetRawAlertTextLen method [Microsoft TV Technologies], GetRawAlertTextLen method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawAlertTextLen method, ISCTE_EAS.GetRawAlertTextLen, ISCTE_EAS::GetRawAlertTextLen, atscpsipparser/ISCTE_EAS::GetRawAlertTextLen, mstv.iscte_eas_getrawalerttextlen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ISCTE_EAS.GetRawAlertTextLen
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::GetRawAlertTextLen


## -description


Gets the length of the alert_text field.


## -parameters




### -param pwVal [out]

Receives the size of the alert_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="https://msdn.microsoft.com/e5ed18e8-e83e-4708-995b-99acd12427a7">ISCTE_EAS::GetRawAlertText</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/4bef1a14-b0f6-40a0-bac0-1d6c00c120e5">ISCTE_EAS::GetAlertText</a>
 

 

