---
UID: NF:strmif.IVMRImagePresenterConfig.SetRenderingPrefs
title: IVMRImagePresenterConfig::SetRenderingPrefs
author: windows-sdk-content
description: The SetRenderingPrefs method sets the rendering preferences on the VMR-7 filter's allocator-presenter.
old-location: dshow\ivmrimagepresenterconfig_setrenderingprefs.htm
tech.root: DirectShow
ms.assetid: 22bb6d52-2201-429d-bd1a-d031c9b017ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRImagePresenterConfig interface [DirectShow],SetRenderingPrefs method, IVMRImagePresenterConfig.SetRenderingPrefs, IVMRImagePresenterConfig::SetRenderingPrefs, IVMRImagePresenterConfigSetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig interface, dshow.ivmrimagepresenterconfig_setrenderingprefs, strmif/IVMRImagePresenterConfig::SetRenderingPrefs
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImagePresenterConfig.SetRenderingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRImagePresenterConfig::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets the rendering preferences on the VMR-7 filter's allocator-presenter.



The VMR-7 filter's <a href="https://msdn.microsoft.com/1374d071-f396-4fcb-8ca2-ac3986960207">IVMRFilterConfig::SetRenderingPrefs</a> method calls through to this method.


## -parameters




### -param dwRenderFlags [in]

A bitwise OR combination of <a href="https://msdn.microsoft.com/cfe1d4a7-b1ec-4d8e-b6d5-3fe5a530c352">VMRRenderPrefs</a> flags that will be used to configure the allocator-presenter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/cbf0fac4-c976-4c1a-ab3a-75ae0d565544">IVMRImagePresenterConfig Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

