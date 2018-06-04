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

# IMFFieldOfUseMFTUnlock::Unlock


## -description


Unlocks a Media Foundation transform (MFT) so that the application can use it.


## -parameters




### -param pUnkMFT [in]

A pointer to the <b>IUnknown</b> interface of the MFT.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method authenticates the caller, using a private communication channel between the MFT and the object that implements the <a href="https://msdn.microsoft.com/b144589b-d559-4686-b617-0e3c393380e9">IMFFieldOfUseMFTUnlock</a> interface. The details of the communication depend entirely on the implementation.




## -see-also




<a href="https://msdn.microsoft.com/36f28e4c-2baf-4618-9935-5d4615f6bc77">Field of Use Restrictions</a>



<a href="https://msdn.microsoft.com/b144589b-d559-4686-b617-0e3c393380e9">IMFFieldOfUseMFTUnlock</a>
 

 

