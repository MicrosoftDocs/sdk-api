---
UID: NF:wmdxva.IWMCodecAMVideoAccelerator.SetAcceleratorInterface
title: IWMCodecAMVideoAccelerator::SetAcceleratorInterface (wmdxva.h)
author: windows-sdk-content
description: The SetAcceleratorInterface method is called by the output pin on the player's source filter to pass the IAMVideoAccelerator interface on the Video Mixing Renderer (VMR) to the decoder DMO.
old-location: wmformat\iwmcodecamvideoaccelerator_setacceleratorinterface.htm
tech.root: wmformat
ms.assetid: 6ffaa2dc-65d6-4ba0-9688-8b59fe593ecd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMCodecAMVideoAccelerator interface [windows Media Format],SetAcceleratorInterface method, IWMCodecAMVideoAccelerator.SetAcceleratorInterface, IWMCodecAMVideoAccelerator::SetAcceleratorInterface, IWMCodecAMVideoAcceleratorSetAcceleratorInterface, SetAcceleratorInterface, SetAcceleratorInterface method [windows Media Format], SetAcceleratorInterface method [windows Media Format],IWMCodecAMVideoAccelerator interface, wmdxva/IWMCodecAMVideoAccelerator::SetAcceleratorInterface, wmformat.iwmcodecamvideoaccelerator_setacceleratorinterface
ms.topic: method
req.header: wmdxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMCodecAMVideoAccelerator.SetAcceleratorInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecAMVideoAccelerator::SetAcceleratorInterface


## -description



The <b>SetAcceleratorInterface</b> method is called by the output pin on the player's source filter to pass the <b>IAMVideoAccelerator</b> interface on the Video Mixing Renderer (VMR) to the decoder <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">DMO</a>.




## -parameters




### -param pIAMVA [in]

Pointer to the <b>IAMVideoAccelerator</b> interface on the VMR.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743308(v=VS.85).aspx">IWMCodecAMVideoAccelerator Interface</a>
 

 

