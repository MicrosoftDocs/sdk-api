---
UID: NF:xapobase.CXAPOParametersBase.EndProcess
title: CXAPOParametersBase::EndProcess (xapobase.h)
author: windows-sdk-content
description: Notifies CXAPOParametersBase that the XAPO has finished accessing the current process parameters.
old-location: xaudio2\cxapoparametersbase_endprocess.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.EndProcess
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],EndProcess method, CXAPOParametersBase.EndProcess, CXAPOParametersBase::EndProcess, EndProcess, EndProcess method [XAudio2 Audio Mixing APIs], EndProcess method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::EndProcess, xaudio2.cxapoparametersbase_endprocess
ms.topic: method
f1_keywords: 
 - "xapobase/CXAPOParametersBase.EndProcess"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CXAPOParametersBase::EndProcess


## -description


Notifies <a href="https://docs.microsoft.com/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a> that the XAPO has finished accessing the current process parameters.


## -parameters






## -returns



This method does not return a value.




## -remarks



XAPOs must call this method within their <a href="https://docs.microsoft.com/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> implementation to access the current process parameters in a thread-safe manner.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a>
 

 

