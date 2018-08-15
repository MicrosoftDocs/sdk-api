---
UID: NF:xapo.IXAPO.LockForProcess
title: IXAPO::LockForProcess
author: windows-sdk-content
description: Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before Process is called on the realtime thread.
old-location: xaudio2\ixapo_interface_lockforprocess.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.LockForProcess(UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS,UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],LockForProcess method, IXAPO.LockForProcess, IXAPO::LockForProcess, LockForProcess, LockForProcess method [XAudio2 Audio Mixing APIs], LockForProcess method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::LockForProcess, xaudio2.ixapo_interface_lockforprocess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.LockForProcess
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPO::LockForProcess


## -description


Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">Process</a> is called on the realtime thread.


## -parameters




### -param InputLockedParameterCount

Number of elements in <i>ppInputLockedParameters</i>. Must be within the <a href="https://msdn.microsoft.com/2824919b-a4ec-4fee-93d2-6157340f2d43">XAPO_REGISTRATION_PROPERTIES</a>.MinInputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxInputBufferCount values passed to <a href="https://msdn.microsoft.com/119EA60F-BB59-4D9A-972F-A95D81EEF765">CXAPOBase::CXAPOBase</a>. 



### -param pInputLockedParameters

Array of input <a href="https://msdn.microsoft.com/23090cfb-ab64-4399-9acb-f4c752a4be1b">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pInputLockedParameters</i> may be NULL if <i>InputLockedParameterCount</i> is 0, otherwise it must have <i>InputLockedParameterCount</i> elements.


### -param OutputLockedParameterCount

Number of elements in ppOutputLockedParameters. Must be within the <a href="https://msdn.microsoft.com/2824919b-a4ec-4fee-93d2-6157340f2d43">XAPO_REGISTRATION_PROPERTIES</a>.MinOutputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxOutputBufferCount values passed to <a href="https://msdn.microsoft.com/119EA60F-BB59-4D9A-972F-A95D81EEF765">CXAPOBase::CXAPOBase</a>. If the XAPO_FLAG_BUFFERCOUNT_MUST_MATCH flag was specified in <b>XAPO_REGISTRATION_PROPERTIES</b>.Flags then <i>OutputLockedParameterCount</i> must equal <i>InputLockedParameterCount</i>.


### -param pOutputLockedParameters

Array of output <a href="https://msdn.microsoft.com/23090cfb-ab64-4399-9acb-f4c752a4be1b">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pOutputLockedParameters</i> may be NULL if <i>OutputLockedParameterCount</i> is 0, otherwise it must have <i>OutputLockedParameterCount</i> elements.


## -returns



Returns S_OK if successful, an error code otherwise.




## -remarks



Once locked, the input and output configuration and any other locked parameters remain constant until <a href="https://msdn.microsoft.com/1D70B361-6EB6-4591-9AD2-2E802F6EE341">UnLockForProcess</a> is called. After an XAPO is locked, further calls to <b>LockForProcess</b> have no effect until the <b>UnLockForProcess</b> function is called.



An XAPO indicates what specific formats it supports through its implementation of the <a href="https://msdn.microsoft.com/3CD26BF0-9EA5-434F-9B97-D375FB6B7D21">IsInputFormatSupported</a> and <a href="https://msdn.microsoft.com/5921C1C2-91DF-4E1F-A179-786CEB997BAF">IsOutputFormatSupported</a> methods. An XAPO should assert the input and output configurations are supported and that any required effect-specific initialization is complete. The <b>IsInputFormatSupported</b>, <b>IsOutputFormatSupported</b>, and <a href="https://msdn.microsoft.com/4C975ED7-5656-4C48-A402-99011B7D37AF">Initialize</a> methods should be used as necessary before calling this method.



Because <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">Process</a> is a nonblocking method, all internal memory buffers required for <b>Process</b> should be allocated in <b>LockForProcess</b>.




<a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">Process</a> is never called before <b>LockForProcess</b> returns successfully.



<b>LockForProcess</b> is called directly by XAudio2 and should not be called by the client code.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/21DA61D2-8EDE-496B-8513-D67121697FBA">IXAPO</a>
 

 

