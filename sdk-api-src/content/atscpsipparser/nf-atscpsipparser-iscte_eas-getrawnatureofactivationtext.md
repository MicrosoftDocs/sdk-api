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

# ISCTE_EAS::GetRawNatureOfActivationText


## -description


Gets the raw nature_of_activation_text field from the EAS table.


## -parameters




### -param pbVal [out]

A pointer to a buffer that receives the nature_of_activation_text field. The caller must allocate the buffer. To get the required size of the buffer, call <a href="https://msdn.microsoft.com/a7f93884-d8a9-449b-afc2-b2ccbd0d2492">ISCTE_EAS::GetRawNatureOfActivationTextLen</a>. The text is formatted as a Multiple String Structure as defined by ATSC PSIP Standard A/65.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the text for a specific language, call <a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>
 

 

