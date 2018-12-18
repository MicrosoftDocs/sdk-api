---
UID: NF:xapobase.CXAPOParametersBase.BeginProcess
title: CXAPOParametersBase::BeginProcess
author: windows-sdk-content
description: Returns the current process parameters.
old-location: xaudio2\cxapoparametersbase_beginprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.BeginProcess
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginProcess, BeginProcess method [XAudio2 Audio Mixing APIs], BeginProcess method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],BeginProcess method, CXAPOParametersBase.BeginProcess, CXAPOParametersBase::BeginProcess, xapobase/CXAPOParametersBase::BeginProcess, xaudio2.cxapoparametersbase_beginprocess
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
 - CXAPOParametersBase.BeginProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CXAPOParametersBase::BeginProcess


## -description


Returns the current process parameters.


## -parameters






## -returns



Returns a pointer to the current process parameters.




## -remarks



XAPOs must call this method within their <a href="https://msdn.microsoft.com/en-us/library/Ee418456(v=VS.85).aspx">IXAPO::Process</a> implementation to access the current process parameters in a thread-safe manner.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415238(v=VS.85).aspx">CXAPOParametersBase</a>
 

 

