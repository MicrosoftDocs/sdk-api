---
UID: NL:xapobase.CXAPOParametersBase
title: CXAPOParametersBase (xapobase.h)
description: Default implementation of the IXAPOParameters interface.
helpviewer_keywords: ["CXAPOParametersBase","CXAPOParametersBase class [XAudio2 Audio Mixing APIs]","CXAPOParametersBase class [XAudio2 Audio Mixing APIs]","described","xapobase/CXAPOParametersBase","xaudio2.cxapoparametersbase"]
old-location: xaudio2\cxapoparametersbase.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase
ms.date: 12/05/2018
ms.keywords: CXAPOParametersBase, CXAPOParametersBase class [XAudio2 Audio Mixing APIs], CXAPOParametersBase class [XAudio2 Audio Mixing APIs],described, xapobase/CXAPOParametersBase, xaudio2.cxapoparametersbase
f1_keywords:
- xapobase/CXAPOParametersBase
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
- CXAPOParametersBase
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CXAPOParametersBase class


## -description


Default implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> interface.

For a list of all members of this class, see <a href="https://docs.microsoft.com/windows/desktop/xaudio2/cxapoparametersbase-members">CXAPOParametersBase Members</a>.


## -remarks



<b>CXAPOParametersBase</b> provides thread-safe, overridable implementations for all <a href="https://docs.microsoft.com/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> methods.



This class is for parameter blocks whose size is larger than 8 bytes. To achieve synchronization of smaller parameter blocks, use Interlocked operations directly on the parameters.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xapobase/nl-xapobase-cxapobase">CXAPOBase</a>



<a href="https://docs.microsoft.com/windows/desktop/xaudio2/cxapoparametersbase-members">CXAPOParametersBase Members</a>



<a href="https://docs.microsoft.com/windows/desktop/xaudio2/classes">Classes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a>
 

 

