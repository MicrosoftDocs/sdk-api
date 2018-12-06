---
UID: NF:mpconfig.IMixerPinConfig.GetStreamTransparent
title: IMixerPinConfig::GetStreamTransparent
author: windows-sdk-content
description: The GetStreamTransparent method determines whether a stream is transparent.
old-location: dshow\imixerpinconfig_getstreamtransparent.htm
tech.root: DirectShow
ms.assetid: adee4565-ccc3-4a72-a4ee-c27980868dfa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStreamTransparent, GetStreamTransparent method [DirectShow], GetStreamTransparent method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetStreamTransparent method, IMixerPinConfig.GetStreamTransparent, IMixerPinConfig::GetStreamTransparent, IMixerPinConfigGetStreamTransparent, dshow.imixerpinconfig_getstreamtransparent, mpconfig/IMixerPinConfig::GetStreamTransparent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMixerPinConfig.GetStreamTransparent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::GetStreamTransparent


## -description



The <code>GetStreamTransparent</code> method determines whether a stream is transparent.




## -parameters




### -param pbStreamTransparent [out]

Pointer to a value indicating whether the stream is transparent. <b>TRUE</b> indicates transparent stream; <b>FALSE</b> indicates not a transparent stream.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/d1f60a35-ffef-4ebb-b331-558772310bcb">IMixerPinConfig::SetStreamTransparent</a>
 

 

