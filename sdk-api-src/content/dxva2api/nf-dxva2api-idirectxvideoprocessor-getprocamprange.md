---
UID: NF:dxva2api.IDirectXVideoProcessor.GetProcAmpRange
title: IDirectXVideoProcessor::GetProcAmpRange (dxva2api.h)
author: windows-sdk-content
description: Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.
old-location: mf\idirectxvideoprocessor_getprocamprange.htm
tech.root: medfound
ms.assetid: e15c8425-7a0b-4d03-b2da-467c800c57c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProcAmpRange, GetProcAmpRange method [Media Foundation], GetProcAmpRange method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetProcAmpRange method, IDirectXVideoProcessor.GetProcAmpRange, IDirectXVideoProcessor::GetProcAmpRange, dxva2api/IDirectXVideoProcessor::GetProcAmpRange, e15c8425-7a0b-4d03-b2da-467c800c57c2, mf.idirectxvideoprocessor_getprocamprange
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectXVideoProcessor::GetProcAmpRange


## -description



Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.




## -parameters




### -param ProcAmpCap [in]

The ProcAmp setting to query. See <a href="https://msdn.microsoft.com/60d97b9e-d77c-4e53-94ea-ebd59c2601df">ProcAmp Settings</a>.


### -param pRange [out]

Pointer to a <a href="https://msdn.microsoft.com/e01328bb-9069-4874-aa35-b3c9bc1c6094">DXVA2_ValueRange</a> structure that receives the range of values for the setting specified in <i>ProcAmpCaps</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
 

 

