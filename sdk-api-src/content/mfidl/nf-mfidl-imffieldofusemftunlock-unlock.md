---
UID: NF:mfidl.IMFFieldOfUseMFTUnlock.Unlock
title: IMFFieldOfUseMFTUnlock::Unlock
author: windows-sdk-content
description: Unlocks a Media Foundation transform (MFT) so that the application can use it.
old-location: mf\imffieldofusemftunlock_unlock.htm
old-project: medfound
ms.assetid: 54b15e72-6551-4162-90ca-a9bed68ca62f
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFFieldOfUseMFTUnlock interface [Media Foundation],Unlock method, IMFFieldOfUseMFTUnlock.Unlock, IMFFieldOfUseMFTUnlock::Unlock, Unlock, Unlock method [Media Foundation], Unlock method [Media Foundation],IMFFieldOfUseMFTUnlock interface, mf.imffieldofusemftunlock_unlock, mfidl/IMFFieldOfUseMFTUnlock::Unlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFFieldOfUseMFTUnlock.Unlock
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

