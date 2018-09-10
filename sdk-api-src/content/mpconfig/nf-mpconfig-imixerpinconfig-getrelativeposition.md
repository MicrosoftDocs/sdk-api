---
UID: NF:mpconfig.IMixerPinConfig.GetRelativePosition
title: IMixerPinConfig::GetRelativePosition
author: windows-sdk-content
description: The GetRelativePosition method retrieves the position of the stream in the display window.
old-location: dshow\imixerpinconfig_getrelativeposition.htm
tech.root: DirectShow
ms.assetid: 0a2bcc3e-361d-4374-9444-717287c07116
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetRelativePosition, GetRelativePosition method [DirectShow], GetRelativePosition method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetRelativePosition method, IMixerPinConfig.GetRelativePosition, IMixerPinConfig::GetRelativePosition, IMixerPinConfigGetRelativePosition, dshow.imixerpinconfig_getrelativeposition, mpconfig/IMixerPinConfig::GetRelativePosition
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
 - IMixerPinConfig.GetRelativePosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::GetRelativePosition


## -description



The <code>GetRelativePosition</code> method retrieves the position of the stream in the display window.




## -parameters




### -param pdwLeft [out]

Pointer to a value indicating the x-coordinate in the top-left corner of the display window.


### -param pdwTop [out]

Pointer to a value indicating the y-coordinate in the top-left corner of the display window.


### -param pdwRight [out]

Pointer to a value indicating the x-coordinate in the bottom-right corner of the display window.


### -param pdwBottom [out]

Pointer to a value indicating the y-coordinate in the bottom-right corner of the display window.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Coordinates not in the {0, 0, 10,000, 10,000} range.

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



This method assumes window coordinates of {0, 0, 10,000, 10,000}. If the video stream is being rendered in the bottom right quarter of the display window, this method would return {5,000, 5,000, 10,000, 10,000}.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/2b8ff58b-04df-4a6a-b501-f5c138b8abbf">IMixerPinConfig::SetRelativePosition</a>
 

 

