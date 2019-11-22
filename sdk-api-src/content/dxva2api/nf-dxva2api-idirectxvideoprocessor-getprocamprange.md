---
UID: NF:dxva2api.IDirectXVideoProcessor.GetProcAmpRange
title: IDirectXVideoProcessor::GetProcAmpRange (dxva2api.h)

description: Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.
old-location: mf\idirectxvideoprocessor_getprocamprange.htm
tech.root: medfound
ms.assetid: e15c8425-7a0b-4d03-b2da-467c800c57c2

ms.date: 12/05/2018
ms.keywords: GetProcAmpRange, GetProcAmpRange method [Media Foundation], GetProcAmpRange method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetProcAmpRange method, IDirectXVideoProcessor.GetProcAmpRange, IDirectXVideoProcessor::GetProcAmpRange, dxva2api/IDirectXVideoProcessor::GetProcAmpRange, e15c8425-7a0b-4d03-b2da-467c800c57c2, mf.idirectxvideoprocessor_getprocamprange
ms.topic: method
f1_keywords:
- dxva2api/IDirectXVideoProcessor.GetProcAmpRange
dev_langs:
 - c++
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxva2api.h
api_name:
- IDirectXVideoProcessor.GetProcAmpRange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectXVideoProcessor::GetProcAmpRange


## -description



Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.




## -parameters




### -param ProcAmpCap [in]

The ProcAmp setting to query. See <a href="https://docs.microsoft.com/windows/desktop/medfound/procamp-settings">ProcAmp Settings</a>.


### -param pRange [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_valuerange">DXVA2_ValueRange</a> structure that receives the range of values for the setting specified in <i>ProcAmpCaps</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>
 

 

