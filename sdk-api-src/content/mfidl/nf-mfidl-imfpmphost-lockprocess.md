---
UID: NF:mfidl.IMFPMPHost.LockProcess
title: IMFPMPHost::LockProcess (mfidl.h)
description: Blocks the protected media path (PMP) process from ending. (IMFPMPHost.LockProcess)
helpviewer_keywords: ["45c533ca-d8ca-43f9-91d2-011a0b0d63a6","IMFPMPHost interface [Media Foundation]","LockProcess method","IMFPMPHost.LockProcess","IMFPMPHost::LockProcess","LockProcess","LockProcess method [Media Foundation]","LockProcess method [Media Foundation]","IMFPMPHost interface","mf.imfpmphost_lockprocess","mfidl/IMFPMPHost::LockProcess"]
old-location: mf\imfpmphost_lockprocess.htm
tech.root: mf
ms.assetid: 45c533ca-d8ca-43f9-91d2-011a0b0d63a6
ms.date: 12/05/2018
ms.keywords: 45c533ca-d8ca-43f9-91d2-011a0b0d63a6, IMFPMPHost interface [Media Foundation],LockProcess method, IMFPMPHost.LockProcess, IMFPMPHost::LockProcess, LockProcess, LockProcess method [Media Foundation], LockProcess method [Media Foundation],IMFPMPHost interface, mf.imfpmphost_lockprocess, mfidl/IMFPMPHost::LockProcess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMPHost::LockProcess
 - mfidl/IMFPMPHost::LockProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFPMPHost.LockProcess
---

# IMFPMPHost::LockProcess


## -description

Blocks the protected media path (PMP) process from ending.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When this method is called, it increments the lock count on the PMP process. For every call to this method, the application should make a corresponding call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-unlockprocess">IMFPMPHost::UnlockProcess</a>, which decrements the lock count. When the PMP process is ready to exit, it waits for about 3 seconds, or until the lock count reaches zero, before exiting.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
