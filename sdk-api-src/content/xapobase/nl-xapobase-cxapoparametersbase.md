---
UID: NL:xapobase.CXAPOParametersBase
title: CXAPOParametersBase
author: windows-sdk-content
description: Default implementation of the IXAPOParameters interface.
old-location: xaudio2\cxapoparametersbase.htm
old-project: xaudio2
ms.assetid: T:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CXAPOParametersBase, CXAPOParametersBase class [XAudio2 Audio Mixing APIs], CXAPOParametersBase class [XAudio2 Audio Mixing APIs],described, xapobase/CXAPOParametersBase, xaudio2.cxapoparametersbase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
 - CXAPOParametersBase
product: Windows
targetos: Windows
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# CXAPOParametersBase class


## -description


Default implementation of the <a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a> interface.

For a list of all members of this class, see <a href="https://msdn.microsoft.com/C2113358-07DE-426E-AF26-BD8ED9902192">CXAPOParametersBase Members</a>.


## -remarks



<b>CXAPOParametersBase</b> provides thread-safe, overridable implementations for all <a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a> methods.



This class is for parameter blocks whose size is larger than 8 bytes. To achieve synchronization of smaller parameter blocks, use Interlocked operations directly on the parameters.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/C55C4597-F379-462E-94FE-D7CF2004D8F4">CXAPOBase</a>



<a href="https://msdn.microsoft.com/C2113358-07DE-426E-AF26-BD8ED9902192">CXAPOParametersBase Members</a>



<a href="https://msdn.microsoft.com/4349f03a-54a0-2780-0138-a893e1568a26">Classes</a>



<a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a>
 

 

