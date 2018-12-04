---
UID: NF:xapobase.CXAPOParametersBase.EndProcess
title: CXAPOParametersBase::EndProcess
author: windows-sdk-content
description: Notifies CXAPOParametersBase that the XAPO has finished accessing the current process parameters.
old-location: xaudio2\cxapoparametersbase_endprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.EndProcess
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],EndProcess method, CXAPOParametersBase.EndProcess, CXAPOParametersBase::EndProcess, EndProcess, EndProcess method [XAudio2 Audio Mixing APIs], EndProcess method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::EndProcess, xaudio2.cxapoparametersbase_endprocess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xapobase.h
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
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOParametersBase.EndProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CXAPOParametersBase::EndProcess


## -description


Notifies <a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a> that the XAPO has finished accessing the current process parameters.


## -parameters






## -returns



This method does not return a value.




## -remarks



XAPOs must call this method within their <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> implementation to access the current process parameters in a thread-safe manner.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a>
 

 

