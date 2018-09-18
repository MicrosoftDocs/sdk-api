---
UID: NF:mfidl.IMFPMPHostApp.LockProcess
title: IMFPMPHostApp::LockProcess
author: windows-sdk-content
description: Blocks the protected media path (PMP) process from ending.
old-location: mf\imfpmphostapp_lockprocess.htm
tech.root: medfound
ms.assetid: ee3da924-a90a-4736-812e-f392631177c2
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFPMPHostApp interface [Media Foundation],LockProcess method, IMFPMPHostApp.LockProcess, IMFPMPHostApp::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPHostApp interface, mf.imfpmphostapp_lockprocess, mfidl/IMFPMPHostApp::LockProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - Mfidl.h
api_name:
 - IMFPMPHostApp.LockProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPHostApp::LockProcess


## -description


Blocks the protected media path (PMP) process from ending.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="https://msdn.microsoft.com/4cb26f53-7d2a-417b-9bb8-0268920cf2a7">IMFPMPHostApp::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.




## -see-also




<a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

