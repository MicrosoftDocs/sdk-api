---
UID: NF:mfidl.IMFPMPHost.LockProcess
title: IMFPMPHost::LockProcess
author: windows-sdk-content
description: Blocks the protected media path (PMP) process from ending.
old-location: mf\imfpmphost_lockprocess.htm
old-project: medfound
ms.assetid: 45c533ca-d8ca-43f9-91d2-011a0b0d63a6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 45c533ca-d8ca-43f9-91d2-011a0b0d63a6, IMFPMPHost interface [Media Foundation],LockProcess method, IMFPMPHost.LockProcess, IMFPMPHost::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPHost interface, mf.imfpmphost_lockprocess, mfidl/IMFPMPHost::LockProcess
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFPMPHost.LockProcess
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPHost::LockProcess


## -description



          Blocks the protected media path (PMP) process from ending.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="https://msdn.microsoft.com/768f4579-5109-4d2b-a93d-f17f6b850c63">IMFPMPHost::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.




## -see-also




<a href="https://msdn.microsoft.com/fab1fb42-07c5-4a74-b6f5-0950b2c3ba46">IMFPMPHost</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

