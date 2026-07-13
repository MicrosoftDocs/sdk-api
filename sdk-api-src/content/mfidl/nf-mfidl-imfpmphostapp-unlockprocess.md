---
UID: NF:mfidl.IMFPMPHostApp.UnlockProcess
title: IMFPMPHostApp::UnlockProcess (mfidl.h)
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPHostApp::LockProcess.
helpviewer_keywords: ["IMFPMPHostApp interface [Media Foundation]","UnlockProcess method","IMFPMPHostApp.UnlockProcess","IMFPMPHostApp::UnlockProcess","UnlockProcess","UnlockProcess method [Media Foundation]","UnlockProcess method [Media Foundation]","IMFPMPHostApp interface","mf.imfpmphostapp_unlockprocess","mfidl/IMFPMPHostApp::UnlockProcess"]
old-location: mf\imfpmphostapp_unlockprocess.htm
tech.root: mf
ms.assetid: 4cb26f53-7d2a-417b-9bb8-0268920cf2a7
ms.date: 12/05/2018
ms.keywords: IMFPMPHostApp interface [Media Foundation],UnlockProcess method, IMFPMPHostApp.UnlockProcess, IMFPMPHostApp::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPHostApp interface, mf.imfpmphostapp_unlockprocess, mfidl/IMFPMPHostApp::UnlockProcess
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
 - IMFPMPHostApp::UnlockProcess
 - mfidl/IMFPMPHostApp::UnlockProcess
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
 - IMFPMPHostApp.UnlockProcess
---

# IMFPMPHostApp::UnlockProcess


## -description

Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-lockprocess">IMFPMPHostApp::LockProcess</a>.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
