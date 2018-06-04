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

# ISCTE_EAS::GetRawNatureOfActivationTextLen


## -description


Gets the length of the nature_of_activation_text field.


## -parameters




### -param pbVal [out]

Receives the size of the nature_of_activation_text field, in bytes. To get the value of the field, allocate a buffer of this size and call <a href="https://msdn.microsoft.com/11ada9ab-b55f-41c1-9d7d-1c856a17a3a9">ISCTE_EAS::GetRawNatureOfActivationText</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS</a>



<a href="https://msdn.microsoft.com/36cb57f1-b894-4c41-b555-db15f8dbe516">ISCTE_EAS::GetNatureOfActivationText</a>
 

 

