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

# IMFTrustedOutput::GetOutputTrustAuthorityByIndex


## -description



          Gets an output trust authority (OTA), specified by index.


## -parameters




### -param dwIndex [in]


            Zero-based index of the OTA to retrieve. To get the number of OTAs provided by this object, call <a href="https://msdn.microsoft.com/3aae6859-0b32-4705-9045-b98d0bbf43a6">IMFTrustedOutput::GetOutputTrustAuthorityCount</a>.
          


### -param ppauthority [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/21594ac0-7e3c-44a3-bbee-64316dd51824">IMFOutputTrustAuthority</a> interface of the OTA. The caller must release the interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a>
 

 

