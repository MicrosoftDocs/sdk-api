---
UID: NF:xapo.IXAPO.LockForProcess
title: IXAPO::LockForProcess (xapo.h)
description: Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before Process is called on the realtime thread.
helpviewer_keywords: ["IXAPO interface [XAudio2 Audio Mixing APIs]","LockForProcess method","IXAPO.LockForProcess","IXAPO::LockForProcess","LockForProcess","LockForProcess method [XAudio2 Audio Mixing APIs]","LockForProcess method [XAudio2 Audio Mixing APIs]","IXAPO interface","xapo/IXAPO::LockForProcess","xaudio2.ixapo_interface_lockforprocess"]
old-location: xaudio2\ixapo_interface_lockforprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.LockForProcess(UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS,UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS)
ms.date: 12/05/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],LockForProcess method, IXAPO.LockForProcess, IXAPO::LockForProcess, LockForProcess, LockForProcess method [XAudio2 Audio Mixing APIs], LockForProcess method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::LockForProcess, xaudio2.ixapo_interface_lockforprocess
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
 - IXAPO::LockForProcess
 - xapo/IXAPO::LockForProcess
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
 - IXAPO.LockForProcess
---

# IXAPO::LockForProcess


## -description

Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a> is called on the realtime thread.

## -parameters

### -param InputLockedParameterCount

Number of elements in <i>ppInputLockedParameters</i>. Must be within the <a href="/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties">XAPO_REGISTRATION_PROPERTIES</a>.MinInputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxInputBufferCount values passed to <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapobase-cxapobase">CXAPOBase::CXAPOBase</a>.

### -param pInputLockedParameters

Array of input <a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pInputLockedParameters</i> may be NULL if <i>InputLockedParameterCount</i> is 0, otherwise it must have <i>InputLockedParameterCount</i> elements.

### -param OutputLockedParameterCount

Number of elements in ppOutputLockedParameters. Must be within the <a href="/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties">XAPO_REGISTRATION_PROPERTIES</a>.MinOutputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxOutputBufferCount values passed to <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapobase-cxapobase">CXAPOBase::CXAPOBase</a>. If the XAPO_FLAG_BUFFERCOUNT_MUST_MATCH flag was specified in <b>XAPO_REGISTRATION_PROPERTIES</b>.Flags then <i>OutputLockedParameterCount</i> must equal <i>InputLockedParameterCount</i>.

### -param pOutputLockedParameters

Array of output <a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pOutputLockedParameters</i> may be NULL if <i>OutputLockedParameterCount</i> is 0, otherwise it must have <i>OutputLockedParameterCount</i> elements.

## -returns

Returns S_OK if successful, an error code otherwise.

## -remarks

Once locked, the input and output configuration and any other locked parameters remain constant until <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-unlockforprocess">UnLockForProcess</a> is called. After an XAPO is locked, further calls to <b>LockForProcess</b> have no effect until the <b>UnLockForProcess</b> function is called.



An XAPO indicates what specific formats it supports through its implementation of the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-isinputformatsupported">IsInputFormatSupported</a> and <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-isoutputformatsupported">IsOutputFormatSupported</a> methods. An XAPO should assert the input and output configurations are supported and that any required effect-specific initialization is complete. The <b>IsInputFormatSupported</b>, <b>IsOutputFormatSupported</b>, and <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-initialize">Initialize</a> methods should be used as necessary before calling this method.



Because <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a> is a nonblocking method, all internal memory buffers required for <b>Process</b> should be allocated in <b>LockForProcess</b>.




<a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a> is never called before <b>LockForProcess</b> returns successfully.



<b>LockForProcess</b> is called directly by XAudio2 and should not be called by the client code.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>