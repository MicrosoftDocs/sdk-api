---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CXAPOParametersBase::OnSetParameters


## -description


Called by <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> to allow for user-defined parameter validation.


## -parameters




### -param pParameters

Effect-specific parameter block.


### -param ParameterByteSize

Size, in bytes, of pParameters.


## -returns



This method does not return a value.




## -remarks



Users are expected to use asserts for parameter validation in <b>OnSetParameters</b>.



The <a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a> class's implementation of <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> validates that <i>ParameterByteSize</i> is equal to the <b>m_uParameterBlockByteSize</b> private member before calling <b>OnSetParameters</b> so it may be assumed that <i>ParameterByteSize</i> == <b>m_uParameterBlockByteSize</b>. <b>m_uParameterBlockByteSize</b> will be equal to the <i>uParameterBlockByteSize</i> parameter passed into the <a href="https://msdn.microsoft.com/08236DB5-8119-4F3F-BB18-D9DCD3713D45">CXAPOParametersBase::CXAPOParametersBase</a> constructor.



This method should not block as it is called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a>
 

 

