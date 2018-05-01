---
UID: NF:xapobase.CXAPOParametersBase.BeginProcess
title: CXAPOParametersBase::BeginProcess method
author: windows-driver-content
description: Returns the current process parameters.
old-location: xaudio2\cxapoparametersbase_beginprocess.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.BeginProcess
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: BeginProcess method [XAudio2 Audio Mixing APIs], BeginProcess method [XAudio2 Audio Mixing APIs], CXAPOParametersBase interface, BeginProcess,CXAPOParametersBase.BeginProcess, CXAPOParametersBase, CXAPOParametersBase interface [XAudio2 Audio Mixing APIs], BeginProcess method, CXAPOParametersBase::BeginProcess, xapobase/CXAPOParametersBase::BeginProcess, xaudio2.cxapoparametersbase_beginprocess
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
req.typenames: XAPO_REGISTRATION_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	XAPOBase.lib
-	XAPOBase.dll
api_name:
-	CXAPOParametersBase.BeginProcess
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOParametersBase::BeginProcess method


## -description


Returns the current process parameters.


## -parameters






## -returns



Returns a pointer to the current process parameters.




## -remarks



XAPOs must call this method within their <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> implementation to access the current process parameters in a thread-safe manner.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a>
 

 

