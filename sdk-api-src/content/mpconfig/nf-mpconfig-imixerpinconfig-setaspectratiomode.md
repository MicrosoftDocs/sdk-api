---
UID: NF:mpconfig.IMixerPinConfig.SetAspectRatioMode
title: IMixerPinConfig::SetAspectRatioMode
author: windows-sdk-content
description: The SetAspectRatioMode method sets the aspect ratio correction mode for window resizing.
old-location: dshow\imixerpinconfig_setaspectratiomode.htm
tech.root: DirectShow
ms.assetid: 907ab0cf-c0a4-4e81-8fb4-90914427d9c0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetAspectRatioMode method, IMixerPinConfig.SetAspectRatioMode, IMixerPinConfig::SetAspectRatioMode, IMixerPinConfigSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setaspectratiomode, mpconfig/IMixerPinConfig::SetAspectRatioMode
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
 - IMixerPinConfig.SetAspectRatioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::SetAspectRatioMode


## -description



The <code>SetAspectRatioMode</code> method sets the aspect ratio correction mode for window resizing.




## -parameters




### -param amAspectRatioMode [in]

Value specifying one of the <a href="https://msdn.microsoft.com/4f7c6220-6231-4bb1-aea6-7f1581b04d3a">AM_ASPECT_RATIO_MODE</a> enumerated type members.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method called on secondary stream.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



Currently this function is implemented only on the primary pin of the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter. Calling it on a secondary pin will result in an error.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/091ebea0-8688-4965-8727-0738cc19d47e">IMixerPinConfig::GetAspectRatioMode</a>
 

 

