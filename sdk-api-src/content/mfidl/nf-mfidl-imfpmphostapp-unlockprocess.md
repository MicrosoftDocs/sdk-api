---
UID: NF:mfidl.IMFPMPHostApp.UnlockProcess
title: IMFPMPHostApp::UnlockProcess
author: windows-driver-content
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPHostApp::LockProcess.
old-location: mf\imfpmphostapp_unlockprocess.htm
old-project: medfound
ms.assetid: 4cb26f53-7d2a-417b-9bb8-0268920cf2a7
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFPMPHostApp interface [Media Foundation],UnlockProcess method, IMFPMPHostApp.UnlockProcess, IMFPMPHostApp::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPHostApp interface, mf.imfpmphostapp_unlockprocess, mfidl/IMFPMPHostApp::UnlockProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mfidl.h
api_name:
-	IMFPMPHostApp.UnlockProcess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPMPHostApp::UnlockProcess


## -description



          Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="https://msdn.microsoft.com/ee3da924-a90a-4736-812e-f392631177c2">IMFPMPHostApp::LockProcess</a>.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

