---
UID: NF:mfidl.IMFPMPHostApp.LockProcess
title: IMFPMPHostApp::LockProcess (mfidl.h)
description: Blocks the protected media path (PMP) process from ending. (IMFPMPHostApp.LockProcess)
helpviewer_keywords: ["IMFPMPHostApp interface [Media Foundation]","LockProcess method","IMFPMPHostApp.LockProcess","IMFPMPHostApp::LockProcess","LockProcess","LockProcess method [Media Foundation]","LockProcess method [Media Foundation]","IMFPMPHostApp interface","mf.imfpmphostapp_lockprocess","mfidl/IMFPMPHostApp::LockProcess"]
old-location: mf\imfpmphostapp_lockprocess.htm
tech.root: mf
ms.assetid: ee3da924-a90a-4736-812e-f392631177c2
ms.date: 12/05/2018
ms.keywords: IMFPMPHostApp interface [Media Foundation],LockProcess method, IMFPMPHostApp.LockProcess, IMFPMPHostApp::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPHostApp interface, mf.imfpmphostapp_lockprocess, mfidl/IMFPMPHostApp::LockProcess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPHostApp::LockProcess
 - mfidl/IMFPMPHostApp::LockProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfidl.h
api_name:
 - IMFPMPHostApp.LockProcess
---

# IMFPMPHostApp::LockProcess


## -description

Blocks the protected media path (PMP) process from ending.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-unlockprocess">IMFPMPHostApp::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
