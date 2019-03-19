---
UID: NF:wmcodecdsp.IWMVideoDecoderHurryup.SetHurryup
title: IWMVideoDecoderHurryup::SetHurryup (wmcodecdsp.h)
author: windows-sdk-content
description: Sets the speed mode of the video decoder.
old-location: mf\iwmvideodecoderhurryupsethurryup.htm
tech.root: medfound
ms.assetid: ef01d2ab-2525-4caf-87d9-3acdc0b3b1b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMVideoDecoderHurryup interface [Media Foundation],SetHurryup method, IWMVideoDecoderHurryup.SetHurryup, IWMVideoDecoderHurryup::SetHurryup, SetHurryup, SetHurryup method [Media Foundation], SetHurryup method [Media Foundation],IWMVideoDecoderHurryup interface, codecapi.iwmvideodecoderhurryupsethurryup, mf.iwmvideodecoderhurryupsethurryup, wmcodecdsp/IWMVideoDecoderHurryup::SetHurryup
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderHurryup.SetHurryup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMVideoDecoderHurryup::SetHurryup


## -description


Sets the speed mode of the video decoder.



## -parameters




### -param lHurryup [in]

The speed mode of the video decoder.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1 (default)</dt>
</dl>
</td>
<td width="60%">
The decoder will determine the decoding speed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The decoder will decode in real time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1 to 4</dt>
</dl>
</td>
<td width="60%">
The decoder will decode faster than real time. The higher the value, the faster the decoding.

</td>
</tr>
</table>
 


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




<a href="https://msdn.microsoft.com/c5c58acd-ebf9-46ce-977b-1478b42559c4">IWMVideoDecoderHurryUp::GetHurryup</a>



<a href="https://msdn.microsoft.com/5e33be5f-5ce8-4f4f-94db-4be2dfcaeec0">IWMVideoDecoderHurryup Interface</a>
 

 

