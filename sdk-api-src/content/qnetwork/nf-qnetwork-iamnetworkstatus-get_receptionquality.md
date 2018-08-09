---
UID: NF:qnetwork.IAMNetworkStatus.get_ReceptionQuality
title: IAMNetworkStatus::get_ReceptionQuality
author: windows-sdk-content
description: The get_ReceptionQuality method retrieves a value indicating the reception quality.
old-location: dshow\iamnetworkstatus_get_receptionquality.htm
old-project: DirectShow
ms.assetid: 6c80f874-c176-4e52-acc9-26c10fac08d9
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMNetworkStatus interface [DirectShow],get_ReceptionQuality method, IAMNetworkStatus.get_ReceptionQuality, IAMNetworkStatus::get_ReceptionQuality, IAMNetworkStatusget_ReceptionQuality, dshow.iamnetworkstatus_get_receptionquality, get_ReceptionQuality, get_ReceptionQuality method [DirectShow], get_ReceptionQuality method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_ReceptionQuality
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetworkStatus.get_ReceptionQuality
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMNetworkStatus::get_ReceptionQuality


## -description



The <code>get_ReceptionQuality</code> method retrieves a value indicating the reception quality.




## -parameters




### -param pReceptionQuality

Pointer to a variable that receives a value from 0 to 100, indicating the reception quality. This value is percentage of packets that the filter received without requiring resending or error correction.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/51d56b76-f9fc-44e1-88f0-d35d861a4697">IAMNetworkStatus Interface</a>
 

 

