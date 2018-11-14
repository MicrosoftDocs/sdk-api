---
UID: NF:atscpsipparser.ISCTE_EAS.GetRawAlertText
title: ISCTE_EAS::GetRawAlertText
author: windows-sdk-content
description: Gets the raw alert_text field from the EAS table.
old-location: mstv\iscte_eas_getrawalerttext.htm
tech.root: MSTV
ms.assetid: e5ed18e8-e83e-4708-995b-99acd12427a7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRawAlertText, GetRawAlertText method [Microsoft TV Technologies], GetRawAlertText method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetRawAlertText method, ISCTE_EAS.GetRawAlertText, ISCTE_EAS::GetRawAlertText, atscpsipparser/ISCTE_EAS::GetRawAlertText, mstv.iscte_eas_getrawalerttext
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
 - ISCTE_EAS.GetRawAlertText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- ISCTE_EAS.GetRawAlertText
: 
---

# ISCTE_EAS::GetRawAlertText


## -description


Gets the raw alert_text field from the EAS table.


## -parameters




### -param pbVal [out]

A pointer to a buffer that receives the alert_text field. The caller must allocate the buffer. To get the required size of the buffer, call <a href="https://msdn.microsoft.com/e85b1deb-6e93-4187-8a18-80740ce9e4c9">ISCTE_EAS::GetRawAlertTextLen</a>. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the alert text for a specific language, call <a href="https://msdn.microsoft.com/4bef1a14-b0f6-40a0-bac0-1d6c00c120e5">ISCTE_EAS::GetAlertText</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/4bef1a14-b0f6-40a0-bac0-1d6c00c120e5">ISCTE_EAS::GetAlertText</a>
 

 

