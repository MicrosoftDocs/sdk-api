---
UID: NF:mftransform.IMFTransform.AddInputStreams
title: IMFTransform::AddInputStreams
author: windows-sdk-content
description: Adds one or more new input streams to this Media Foundation transform (MFT).
old-location: mf\imftransform_addinputstreams.htm
tech.root: medfound
ms.assetid: 311ab66e-5dbd-452a-bad4-99a6293cbc60
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 311ab66e-5dbd-452a-bad4-99a6293cbc60, AddInputStreams, AddInputStreams method [Media Foundation], AddInputStreams method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],AddInputStreams method, IMFTransform.AddInputStreams, IMFTransform::AddInputStreams, mf.imftransform_addinputstreams, mftransform/IMFTransform::AddInputStreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.AddInputStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::AddInputStreams


## -description


Adds one or more new input streams to this Media Foundation transform (MFT).
        


## -parameters




### -param cStreams [in]

Number of streams to add.
          


### -param adwStreamIDs [in]

Array of stream identifiers. The new stream identifiers must not match any existing input streams.
          


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
Invalid argument.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The MFT has a fixed number of input streams.
              

</td>
</tr>
</table>
 




## -remarks



If the new streams exceed the maximum number of input streams for this transform, the method returns <b>E_INVALIDARG.</b> To find the maximum number of input streams, call <a href="https://msdn.microsoft.com/4d9585f0-5818-4e7f-925c-4c50ae6a6edc">IMFTransform::GetStreamLimits</a>.
      

If any of the new stream identifiers conflicts with an existing input stream, the method returns <b>E_INVALIDARG</b>.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTAddInputStreams</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

