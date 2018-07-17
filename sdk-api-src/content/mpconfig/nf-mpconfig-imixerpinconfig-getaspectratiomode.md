---
UID: NF:mpconfig.IMixerPinConfig.GetAspectRatioMode
title: IMixerPinConfig::GetAspectRatioMode
author: windows-sdk-content
description: The GetAspectRatioMode method retrieves the aspect ratio correction mode for window resizing.
old-location: dshow\imixerpinconfig_getaspectratiomode.htm
old-project: DirectShow
ms.assetid: 091ebea0-8688-4965-8727-0738cc19d47e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetAspectRatioMode method, IMixerPinConfig.GetAspectRatioMode, IMixerPinConfig::GetAspectRatioMode, IMixerPinConfigGetAspectRatioMode, dshow.imixerpinconfig_getaspectratiomode, mpconfig/IMixerPinConfig::GetAspectRatioMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AM_ASPECT_RATIO_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig.GetAspectRatioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method retrieves the aspect ratio correction mode for window resizing.




## -parameters




### -param pamAspectRatioMode [out]

Pointer to an <a href="https://msdn.microsoft.com/4f7c6220-6231-4bb1-aea6-7f1581b04d3a">AM_ASPECT_RATIO_MODE</a> enumerated type member.


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
Value invalid or <b>NULL</b>.

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



<a href="https://msdn.microsoft.com/907ab0cf-c0a4-4e81-8fb4-90914427d9c0">IMixerPinConfig::SetAspectRatioMode</a>
 

 

