---
UID: NF:mpconfig.IMixerPinConfig.GetAspectRatioMode
title: IMixerPinConfig::GetAspectRatioMode (mpconfig.h)
description: The GetAspectRatioMode method retrieves the aspect ratio correction mode for window resizing.
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [DirectShow]","GetAspectRatioMode method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetAspectRatioMode method","IMixerPinConfig.GetAspectRatioMode","IMixerPinConfig::GetAspectRatioMode","IMixerPinConfigGetAspectRatioMode","dshow.imixerpinconfig_getaspectratiomode","mpconfig/IMixerPinConfig::GetAspectRatioMode"]
old-location: dshow\imixerpinconfig_getaspectratiomode.htm
tech.root: dshow
ms.assetid: 091ebea0-8688-4965-8727-0738cc19d47e
ms.date: 12/05/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetAspectRatioMode method, IMixerPinConfig.GetAspectRatioMode, IMixerPinConfig::GetAspectRatioMode, IMixerPinConfigGetAspectRatioMode, dshow.imixerpinconfig_getaspectratiomode, mpconfig/IMixerPinConfig::GetAspectRatioMode
f1_keywords:
- mpconfig/IMixerPinConfig.GetAspectRatioMode
dev_langs:
- c++
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
- IMixerPinConfig.GetAspectRatioMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerPinConfig::GetAspectRatioMode


## -description



The <code>GetAspectRatioMode</code> method retrieves the aspect ratio correction mode for window resizing.




## -parameters




### -param pamAspectRatioMode [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/ne-mpconfig-am_aspect_ratio_mode">AM_ASPECT_RATIO_MODE</a> enumerated type member.


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setaspectratiomode">IMixerPinConfig::SetAspectRatioMode</a>
 

 

