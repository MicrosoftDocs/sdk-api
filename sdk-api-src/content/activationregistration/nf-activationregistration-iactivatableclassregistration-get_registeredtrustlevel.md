---
UID: NF:activationregistration.IActivatableClassRegistration.get_RegisteredTrustLevel
title: IActivatableClassRegistration::get_RegisteredTrustLevel
author: windows-sdk-content
description: Gets the trust level of the current activatable class.
old-location: winrt\iactivatableclassregistration_registeredtrustlevel.htm
tech.root: WinRT
ms.assetid: 3DFE773C-CF63-489A-988B-2FFF4215C8BF
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IActivatableClassRegistration interface [Windows Runtime],get_RegisteredTrustLevel method, IActivatableClassRegistration.get_RegisteredTrustLevel, IActivatableClassRegistration::get_RegisteredTrustLevel, activationregistration/IActivatableClassRegistration::get_RegisteredTrustLevel, get_RegisteredTrustLevel, get_RegisteredTrustLevel method [Windows Runtime], get_RegisteredTrustLevel method [Windows Runtime],IActivatableClassRegistration interface, winrt.iactivatableclassregistration_registeredtrustlevel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: activationregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - activationregistration.h
api_name:
 - IActivatableClassRegistration.get_RegisteredTrustLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActivatableClassRegistration::get_RegisteredTrustLevel


## -description


Gets the trust level of the current activatable class.


## -parameters




### -param registeredTrustLevel [out, retval]

The trust level of the current activatable class.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/99834A2D-547B-4B04-8703-46B11E0BB812">IActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/1B579206-F6B9-47C1-A7F3-4E7ECDEDCBB4">RegisteredTrustLevel</a>



<a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a>
 

 

