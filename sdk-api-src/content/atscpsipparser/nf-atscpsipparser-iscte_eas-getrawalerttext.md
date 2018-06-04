---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

