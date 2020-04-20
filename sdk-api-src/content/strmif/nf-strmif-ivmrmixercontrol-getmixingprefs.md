---
UID: NF:strmif.IVMRMixerControl.GetMixingPrefs
title: IVMRMixerControl::GetMixingPrefs (strmif.h)
description: Retrieves the mixing preferences for the stream.helpviewer_keywords: ["GetMixingPrefs","GetMixingPrefs method [DirectShow]","GetMixingPrefs method [DirectShow]","IVMRMixerControl interface","IVMRMixerControl interface [DirectShow]","GetMixingPrefs method","IVMRMixerControl.GetMixingPrefs","IVMRMixerControl::GetMixingPrefs","IVMRMixerControlGetMixingPrefs","dshow.ivmrmixercontrol_getmixingprefs","strmif/IVMRMixerControl::GetMixingPrefs"]
old-location: dshow\ivmrmixercontrol_getmixingprefs.htm
tech.root: DirectShow
ms.assetid: ee410a7e-e021-408a-bf40-cb58dc8eca1c
ms.date: 12/05/2018
ms.keywords: GetMixingPrefs, GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetMixingPrefs method, IVMRMixerControl.GetMixingPrefs, IVMRMixerControl::GetMixingPrefs, IVMRMixerControlGetMixingPrefs, dshow.ivmrmixercontrol_getmixingprefs, strmif/IVMRMixerControl::GetMixingPrefs
f1_keywords:
- strmif/IVMRMixerControl.GetMixingPrefs
dev_langs:
- c++
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
- IVMRMixerControl.GetMixingPrefs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl::GetMixingPrefs


## -description



Retrieves the mixing preferences for the stream.




## -parameters




### -param pdwMixerPrefs [in]

Address of a variable that receives a bitwise OR combination of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-vmrmixerprefs">VMRMixerPrefs</a> flags.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

