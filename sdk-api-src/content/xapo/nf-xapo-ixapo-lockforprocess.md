---
UID: NF:xapo.IXAPO.LockForProcess
title: IXAPO::LockForProcess (xapo.h)
author: windows-sdk-content
description: Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before Process is called on the realtime thread.
old-location: xaudio2\ixapo_interface_lockforprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.LockForProcess(UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS,UINT32,const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXAPO interface [XAudio2 Audio Mixing APIs],LockForProcess method, IXAPO.LockForProcess, IXAPO::LockForProcess, LockForProcess, LockForProcess method [XAudio2 Audio Mixing APIs], LockForProcess method [XAudio2 Audio Mixing APIs],IXAPO interface, xapo/IXAPO::LockForProcess, xaudio2.ixapo_interface_lockforprocess
ms.topic: method
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
req.typenames: 
req.redist: 
---

# IXAPO::LockForProcess


## -description


Called by XAudio2 to lock the input and output configurations of an XAPO allowing it to do any final initialization before <a href="https://msdn.microsoft.com/en-us/library/Ee418456(v=VS.85).aspx">Process</a> is called on the realtime thread.


## -parameters




### -param InputLockedParameterCount

Number of elements in <i>ppInputLockedParameters</i>. Must be within the <a href="https://msdn.microsoft.com/en-us/library/Ee419210(v=VS.85).aspx">XAPO_REGISTRATION_PROPERTIES</a>.MinInputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxInputBufferCount values passed to <a href="https://msdn.microsoft.com/en-us/library/Ee416373(v=VS.85).aspx">CXAPOBase::CXAPOBase</a>. 



### -param pInputLockedParameters

Array of input <a href="https://msdn.microsoft.com/en-us/library/Ee419208(v=VS.85).aspx">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pInputLockedParameters</i> may be NULL if <i>InputLockedParameterCount</i> is 0, otherwise it must have <i>InputLockedParameterCount</i> elements.


### -param OutputLockedParameterCount

Number of elements in ppOutputLockedParameters. Must be within the <a href="https://msdn.microsoft.com/en-us/library/Ee419210(v=VS.85).aspx">XAPO_REGISTRATION_PROPERTIES</a>.MinOutputBufferCount and <b>XAPO_REGISTRATION_PROPERTIES</b>.MaxOutputBufferCount values passed to <a href="https://msdn.microsoft.com/en-us/library/Ee416373(v=VS.85).aspx">CXAPOBase::CXAPOBase</a>. If the XAPO_FLAG_BUFFERCOUNT_MUST_MATCH flag was specified in <b>XAPO_REGISTRATION_PROPERTIES</b>.Flags then <i>OutputLockedParameterCount</i> must equal <i>InputLockedParameterCount</i>.


### -param pOutputLockedParameters

Array of output <a href="https://msdn.microsoft.com/en-us/library/Ee419208(v=VS.85).aspx">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structures. <i>pOutputLockedParameters</i> may be NULL if <i>OutputLockedParameterCount</i> is 0, otherwise it must have <i>OutputLockedParameterCount</i> elements.


## -returns



Returns S_OK if successful, an error code otherwise.




## -remarks



Once locked, the input and output configuration and any other locked parameters remain constant until <a href="https://msdn.microsoft.com/en-us/library/Ee418460(v=VS.85).aspx">UnLockForProcess</a> is called. After an XAPO is locked, further calls to <b>LockForProcess</b> have no effect until the <b>UnLockForProcess</b> function is called.



An XAPO indicates what specific formats it supports through its implementation of the <a href="https://msdn.microsoft.com/en-us/library/Ee418453(v=VS.85).aspx">IsInputFormatSupported</a> and <a href="https://msdn.microsoft.com/en-us/library/Ee418454(v=VS.85).aspx">IsOutputFormatSupported</a> methods. An XAPO should assert the input and output configurations are supported and that any required effect-specific initialization is complete. The <b>IsInputFormatSupported</b>, <b>IsOutputFormatSupported</b>, and <a href="https://msdn.microsoft.com/en-us/library/Ee418452(v=VS.85).aspx">Initialize</a> methods should be used as necessary before calling this method.



Because <a href="https://msdn.microsoft.com/en-us/library/Ee418456(v=VS.85).aspx">Process</a> is a nonblocking method, all internal memory buffers required for <b>Process</b> should be allocated in <b>LockForProcess</b>.




<a href="https://msdn.microsoft.com/en-us/library/Ee418456(v=VS.85).aspx">Process</a> is never called before <b>LockForProcess</b> returns successfully.



<b>LockForProcess</b> is called directly by XAudio2 and should not be called by the client code.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a>
 

 

