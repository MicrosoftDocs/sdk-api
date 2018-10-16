---
UID: NF:mfidl.IMFPMPHost.UnlockProcess
title: IMFPMPHost::UnlockProcess
author: windows-sdk-content
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPHost::LockProcess.
old-location: mf\imfpmphost_unlockprocess.htm
tech.root: medfound
ms.assetid: 768f4579-5109-4d2b-a93d-f17f6b850c63
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 768f4579-5109-4d2b-a93d-f17f6b850c63, IMFPMPHost interface [Media Foundation],UnlockProcess method, IMFPMPHost.UnlockProcess, IMFPMPHost::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPHost interface, mf.imfpmphost_unlockprocess, mfidl/IMFPMPHost::UnlockProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPHost.UnlockProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPHost::UnlockProcess


## -description


Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="https://msdn.microsoft.com/45c533ca-d8ca-43f9-91d2-011a0b0d63a6">IMFPMPHost::LockProcess</a>.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

