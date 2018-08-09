---
UID: NF:strmif.IVMRMixerBitmap.UpdateAlphaBitmapParameters
title: IVMRMixerBitmap::UpdateAlphaBitmapParameters
author: windows-sdk-content
description: The UpdateAlphaBitmapParameters method changes the bitmap location, size and blending value.
old-location: dshow\ivmrmixerbitmap_updatealphabitmapparameters.htm
old-project: DirectShow
ms.assetid: 039cb675-c384-4909-b06d-b331cc281df6
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVMRMixerBitmap interface [DirectShow],UpdateAlphaBitmapParameters method, IVMRMixerBitmap.UpdateAlphaBitmapParameters, IVMRMixerBitmap::UpdateAlphaBitmapParameters, IVMRMixerBitmapUpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters method [DirectShow], UpdateAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap interface, dshow.ivmrmixerbitmap_updatealphabitmapparameters, strmif/IVMRMixerBitmap::UpdateAlphaBitmapParameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IVMRMixerBitmap.UpdateAlphaBitmapParameters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerBitmap::UpdateAlphaBitmapParameters


## -description



The <b>UpdateAlphaBitmapParameters</b> method changes the bitmap location, size and blending value.




## -parameters




### -param pBmpParms [in]

A pointer to a <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure.
          


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The filter graph must be running for the changes to take effect. This method does not change the bitmap image. If you specify a <a href="https://msdn.microsoft.com/03b3e619-4804-42de-88d5-5422089e875a">VMRALPHABITMAP</a> structure with no destination or color key set, the bitmap disappears. This behavior is by design for backward compatibility and cannot be changed.
      




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ac7da3f9-2c17-4517-bb64-6b56257a65c3">IVMRMixerBitmap Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a>
 

 

