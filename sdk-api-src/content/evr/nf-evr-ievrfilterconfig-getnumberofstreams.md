---
UID: NF:evr.IEVRFilterConfig.GetNumberOfStreams
title: IEVRFilterConfig::GetNumberOfStreams
author: windows-sdk-content
description: Retrieves the number of input pins on the EVR filter. The EVR filter always has at least one input pin, which corresponds to the reference stream.
old-location: mf\ievrfilterconfig_getnumberofstreams.htm
old-project: medfound
ms.assetid: 94e15032-efb6-4919-b018-953eee803135
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 94e15032-efb6-4919-b018-953eee803135, GetNumberOfStreams, GetNumberOfStreams method [Media Foundation], GetNumberOfStreams method [Media Foundation],IEVRFilterConfig interface, IEVRFilterConfig interface [Media Foundation],GetNumberOfStreams method, IEVRFilterConfig.GetNumberOfStreams, IEVRFilterConfig::GetNumberOfStreams, evr/IEVRFilterConfig::GetNumberOfStreams, mf.ievrfilterconfig_getnumberofstreams
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRFilterConfig.GetNumberOfStreams
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEVRFilterConfig::GetNumberOfStreams


## -description



Retrieves the number of input pins on the EVR filter. The EVR filter always has at least one input pin, which corresponds to the reference stream.




## -parameters




### -param pdwMaxStreams [out]

Receives the number of streams.


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




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/13086d85-3dbf-4e9f-b065-d95e16412832">IEVRFilterConfig</a>
 

 

