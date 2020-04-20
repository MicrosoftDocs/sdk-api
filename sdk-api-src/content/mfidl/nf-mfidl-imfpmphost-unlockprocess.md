---
UID: NF:mfidl.IMFPMPHost.UnlockProcess
title: IMFPMPHost::UnlockProcess (mfidl.h)
description: Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to IMFPMPHost::LockProcess.helpviewer_keywords: ["768f4579-5109-4d2b-a93d-f17f6b850c63","IMFPMPHost interface [Media Foundation]","UnlockProcess method","IMFPMPHost.UnlockProcess","IMFPMPHost::UnlockProcess","UnlockProcess","UnlockProcess method [Media Foundation]","UnlockProcess method [Media Foundation]","IMFPMPHost interface","mf.imfpmphost_unlockprocess","mfidl/IMFPMPHost::UnlockProcess"]
old-location: mf\imfpmphost_unlockprocess.htm
tech.root: medfound
ms.assetid: 768f4579-5109-4d2b-a93d-f17f6b850c63
ms.date: 12/05/2018
ms.keywords: 768f4579-5109-4d2b-a93d-f17f6b850c63, IMFPMPHost interface [Media Foundation],UnlockProcess method, IMFPMPHost.UnlockProcess, IMFPMPHost::UnlockProcess, UnlockProcess, UnlockProcess method [Media Foundation], UnlockProcess method [Media Foundation],IMFPMPHost interface, mf.imfpmphost_unlockprocess, mfidl/IMFPMPHost::UnlockProcess
f1_keywords:
- mfidl/IMFPMPHost.UnlockProcess
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPHost::UnlockProcess


## -description


Decrements the lock count on the protected media path (PMP) process. Call this method once for each call to <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-lockprocess">IMFPMPHost::LockProcess</a>.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphost">IMFPMPHost</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

