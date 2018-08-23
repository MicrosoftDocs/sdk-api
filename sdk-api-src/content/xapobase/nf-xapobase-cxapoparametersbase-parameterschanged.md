---
UID: NF:xapobase.CXAPOParametersBase.ParametersChanged
title: CXAPOParametersBase::ParametersChanged
author: windows-sdk-content
description: Indicates if IXAPOParameters::SetParameters has been called since the last processing pass.
old-location: xaudio2\cxapoparametersbase_parameterschanged.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.ParametersChanged
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],ParametersChanged method, CXAPOParametersBase.ParametersChanged, CXAPOParametersBase::ParametersChanged, ParametersChanged, ParametersChanged method [XAudio2 Audio Mixing APIs], ParametersChanged method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::ParametersChanged, xaudio2.cxapoparametersbase_parameterschanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapobase.h
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
req.typenames: XAPO_REGISTRATION_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOParametersBase.ParametersChanged
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOParametersBase::ParametersChanged


## -description


Indicates if <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> has been called since the last processing pass.


## -parameters






## -returns



Returns TRUE if <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> has been called since the last processing pass. May only be used within the XAPO's <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> implementation, before <a href="https://msdn.microsoft.com/BC386533-FD78-4CE5-8CE7-E156EE92D500">CXAPOParametersBase::BeginProcess</a> is called. 




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a>
 

 

