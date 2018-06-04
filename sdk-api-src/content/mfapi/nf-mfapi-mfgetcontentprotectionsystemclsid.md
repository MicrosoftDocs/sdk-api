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

# MFGetContentProtectionSystemCLSID function


## -description


Gets the class identifier for a content protection system.


## -parameters




### -param guidProtectionSystemID [in]

The GUID that identifies the content protection system.


### -param pclsid [out]

Receives the class identifier to the content protection system.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The class identifier can be used to create the input trust authority (ITA) for the content protection system. Call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> or <a href="https://msdn.microsoft.com/787fc392-1858-41f4-a1ce-2da02a5e789f">IMFPMPHost::CreateObjectByCLSID</a> to get an <a href="https://msdn.microsoft.com/59a9def7-69a6-4f80-bb5e-1cb372ff6eab">IMFTrustedInput</a>  pointer.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

