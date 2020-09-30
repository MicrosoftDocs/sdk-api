---
UID: NF:strmif.IVMRMixerControl.GetBackgroundClr
title: IVMRMixerControl::GetBackgroundClr (strmif.h)
description: Gets the current background color on the output rectangle.
helpviewer_keywords: ["GetBackgroundClr","GetBackgroundClr method [DirectShow]","GetBackgroundClr method [DirectShow]","IVMRMixerControl interface","IVMRMixerControl interface [DirectShow]","GetBackgroundClr method","IVMRMixerControl.GetBackgroundClr","IVMRMixerControl::GetBackgroundClr","IVMRMixerControlGetBackgroundClr","dshow.ivmrmixercontrol_getbackgroundclr","strmif/IVMRMixerControl::GetBackgroundClr"]
old-location: dshow\ivmrmixercontrol_getbackgroundclr.htm
tech.root: dshow
ms.assetid: 095f0ed3-46e4-48f9-97d5-5bca1c2efa30
ms.date: 12/05/2018
ms.keywords: GetBackgroundClr, GetBackgroundClr method [DirectShow], GetBackgroundClr method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetBackgroundClr method, IVMRMixerControl.GetBackgroundClr, IVMRMixerControl::GetBackgroundClr, IVMRMixerControlGetBackgroundClr, dshow.ivmrmixercontrol_getbackgroundclr, strmif/IVMRMixerControl::GetBackgroundClr
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRMixerControl::GetBackgroundClr
 - strmif/IVMRMixerControl::GetBackgroundClr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRMixerControl.GetBackgroundClr
---

# IVMRMixerControl::GetBackgroundClr


## -description

Gets the current background color on the output rectangle.

## -parameters

### -param lpClrBkg [in]

Address of a variable that receives the background color.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>