---
UID: NF:evr.IEVRFilterConfig.SetNumberOfStreams
title: IEVRFilterConfig::SetNumberOfStreams
author: windows-sdk-content
description: Sets the number of input pins on the EVR filter.
old-location: mf\ievrfilterconfig_setnumberofstreams.htm
tech.root: MedFound
ms.assetid: 72777c3d-b098-43b9-80ea-ef180b7f1a4a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 72777c3d-b098-43b9-80ea-ef180b7f1a4a, IEVRFilterConfig interface [Media Foundation],SetNumberOfStreams method, IEVRFilterConfig.SetNumberOfStreams, IEVRFilterConfig::SetNumberOfStreams, SetNumberOfStreams, SetNumberOfStreams method [Media Foundation], SetNumberOfStreams method [Media Foundation],IEVRFilterConfig interface, evr/IEVRFilterConfig::SetNumberOfStreams, mf.ievrfilterconfig_setnumberofstreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: evr.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRFilterConfig.SetNumberOfStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEVRFilterConfig::SetNumberOfStreams


## -description



Sets the number of input pins on the EVR filter.




## -parameters




### -param dwMaxStreams [in]

Specifies the total number of input pins on the EVR filter. This value includes the input pin for the reference stream, which is created by default. For example, to mix one substream plus the reference stream, set this parameter to 2.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid number of streams. The minimum is one, and the maximum is 16.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
This method has already been called, or at least one pin is already connected.

</td>
</tr>
</table>
 




## -remarks



After this method has been called, it cannot be called a second time on the same instance of the EVR filter. Also, the method fails if any input pins are connected.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/13086d85-3dbf-4e9f-b065-d95e16412832">IEVRFilterConfig</a>
 

 

