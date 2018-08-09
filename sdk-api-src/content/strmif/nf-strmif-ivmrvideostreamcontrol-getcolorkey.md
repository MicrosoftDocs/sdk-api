---
UID: NF:strmif.IVMRVideoStreamControl.GetColorKey
title: IVMRVideoStreamControl::GetColorKey
author: windows-sdk-content
description: The GetColorKey method retrieves the source color key currently set for this stream.
old-location: dshow\ivmrvideostreamcontrol_getcolorkey.htm
old-project: DirectShow
ms.assetid: 2075ac12-c799-4716-994f-46ff6928e670
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IVMRVideoStreamControl interface, IVMRVideoStreamControl interface [DirectShow],GetColorKey method, IVMRVideoStreamControl.GetColorKey, IVMRVideoStreamControl::GetColorKey, IVMRVideoStreamControlGetColorKey, dshow.ivmrvideostreamcontrol_getcolorkey, strmif/IVMRVideoStreamControl::GetColorKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRVideoStreamControl.GetColorKey
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRVideoStreamControl::GetColorKey


## -description



The <code>GetColorKey</code> method retrieves the source color key currently set for this stream.




## -parameters




### -param lpClrKey






#### - pclr [out]

Address of a <a href="https://msdn.microsoft.com/bd360860-94e3-4f91-a455-5fdb227368b3">DDCOLORKEY</a> structure that receives the source color key.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b42fa81e-99d7-4051-b909-2189581825d0">IVMRVideoStreamControl Interface</a>



<a href="https://msdn.microsoft.com/30a4009c-5da0-4a07-9d4b-7c9047fb6dd8">IVMRVideoStreamControl::SetColorKey</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

