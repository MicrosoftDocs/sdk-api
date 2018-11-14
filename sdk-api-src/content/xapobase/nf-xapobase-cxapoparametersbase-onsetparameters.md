---
UID: NF:xapobase.CXAPOParametersBase.OnSetParameters
title: CXAPOParametersBase::OnSetParameters
author: windows-sdk-content
description: Called by IXAPOParameters::SetParameters to allow for user-defined parameter validation.
old-location: xaudio2\cxapoparametersbase_onsetparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.OnSetParameters(const void,UINT32)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],OnSetParameters method, CXAPOParametersBase.OnSetParameters, CXAPOParametersBase::OnSetParameters, OnSetParameters, OnSetParameters method [XAudio2 Audio Mixing APIs], OnSetParameters method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, xapobase/CXAPOParametersBase::OnSetParameters, xaudio2.cxapoparametersbase_onsetparameters
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
 - CXAPOParametersBase.OnSetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xapobase.h
: 
- CXAPOParametersBase.OnSetParameters
: 
---

# CXAPOParametersBase::OnSetParameters


## -description


Called by <a href="https://msdn.microsoft.com/en-us/library/Ee418447(v=VS.85).aspx">IXAPOParameters::SetParameters</a> to allow for user-defined parameter validation.


## -parameters




### -param pParameters

Effect-specific parameter block.


### -param ParameterByteSize

Size, in bytes, of pParameters.


## -returns



This method does not return a value.




## -remarks



Users are expected to use asserts for parameter validation in <b>OnSetParameters</b>.



The <a href="https://msdn.microsoft.com/en-us/library/Ee415238(v=VS.85).aspx">CXAPOParametersBase</a> class's implementation of <a href="https://msdn.microsoft.com/en-us/library/Ee418447(v=VS.85).aspx">IXAPOParameters::SetParameters</a> validates that <i>ParameterByteSize</i> is equal to the <b>m_uParameterBlockByteSize</b> private member before calling <b>OnSetParameters</b> so it may be assumed that <i>ParameterByteSize</i> == <b>m_uParameterBlockByteSize</b>. <b>m_uParameterBlockByteSize</b> will be equal to the <i>uParameterBlockByteSize</i> parameter passed into the <a href="https://msdn.microsoft.com/en-us/library/Ee416386(v=VS.85).aspx">CXAPOParametersBase::CXAPOParametersBase</a> constructor.



This method should not block as it is called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415238(v=VS.85).aspx">CXAPOParametersBase</a>
 

 

