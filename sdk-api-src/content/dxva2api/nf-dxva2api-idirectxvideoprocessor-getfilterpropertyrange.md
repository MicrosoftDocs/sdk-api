---
UID: NF:dxva2api.IDirectXVideoProcessor.GetFilterPropertyRange
title: IDirectXVideoProcessor::GetFilterPropertyRange
author: windows-sdk-content
description: Retrieves the range of values for an image filter supported by this device.
old-location: mf\idirectxvideoprocessor_getfilterpropertyrange.htm
tech.root: medfound
ms.assetid: 550c426b-a194-4ed6-9a90-b79a93e79322
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 550c426b-a194-4ed6-9a90-b79a93e79322, GetFilterPropertyRange, GetFilterPropertyRange method [Media Foundation], GetFilterPropertyRange method [Media Foundation],IDirectXVideoProcessor interface, IDirectXVideoProcessor interface [Media Foundation],GetFilterPropertyRange method, IDirectXVideoProcessor.GetFilterPropertyRange, IDirectXVideoProcessor::GetFilterPropertyRange, dxva2api/IDirectXVideoProcessor::GetFilterPropertyRange, mf.idirectxvideoprocessor_getfilterpropertyrange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirectXVideoProcessor.GetFilterPropertyRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxva2api.h
: 
- IDirectXVideoProcessor.GetFilterPropertyRange
: 
---

# IDirectXVideoProcessor::GetFilterPropertyRange


## -description



Retrieves the range of values for an image filter supported by this device.




## -parameters




### -param FilterSetting [in]

Filter setting to query. For more information, see <a href="https://msdn.microsoft.com/6514992e-8188-4d28-879c-547e9b340b28">DXVA Image Filter Settings</a>.


### -param pRange [out]

Pointer to a <a href="https://msdn.microsoft.com/e01328bb-9069-4874-aa35-b3c9bc1c6094">DXVA2_ValueRange</a> structure that receives the range of values for the setting specified in <i>FilterSetting</i>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5">IDirectXVideoProcessor</a>
 

 

