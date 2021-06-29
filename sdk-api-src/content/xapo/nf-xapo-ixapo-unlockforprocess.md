---
UID: NF:xapo.IXAPO.UnlockForProcess
title: IXAPO::UnlockForProcess (xapo.h)
description: Deallocates variables that were allocated with the LockForProcess method.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","UnlockForProcess method","IXAPO.UnlockForProcess","IXAPO::UnlockForProcess","UnlockForProcess","UnlockForProcess method [XAudio2 Audio Mixing APIs]","UnlockForProcess method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::UnlockForProcess","xaudio2.ixapo_interface_unlockforprocess"]
old-location: xaudio2\ixapo_interface_unlockforprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.UnlockForProcess
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],UnlockForProcess method, IXAPO.UnlockForProcess, IXAPO::UnlockForProcess, UnlockForProcess, UnlockForProcess method [XAudio2 Audio Mixing APIs], UnlockForProcess method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::UnlockForProcess, xaudio2.ixapo_interface_unlockforprocess
req.header: xapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IXAPO::UnlockForProcess
 - xapo/IXAPO::UnlockForProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.UnlockForProcess
---

# IXAPO::UnlockForProcess


## -description

Deallocates variables that were allocated with the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">LockForProcess</a> method.



## -remarks

Unlocking an XAPO instance allows it to be reused with different input and output formats.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>
