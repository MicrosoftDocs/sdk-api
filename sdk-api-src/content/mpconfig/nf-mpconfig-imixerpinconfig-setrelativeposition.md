---
UID: NF:mpconfig.IMixerPinConfig.SetRelativePosition
title: IMixerPinConfig::SetRelativePosition
author: windows-sdk-content
description: The SetRelativePosition method sets the position of the stream in the display window.
old-location: dshow\imixerpinconfig_setrelativeposition.htm
old-project: DirectShow
ms.assetid: 2b8ff58b-04df-4a6a-b501-f5c138b8abbf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetRelativePosition method, IMixerPinConfig.SetRelativePosition, IMixerPinConfig::SetRelativePosition, IMixerPinConfigSetRelativePosition, SetRelativePosition, SetRelativePosition method [DirectShow], SetRelativePosition method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setrelativeposition, mpconfig/IMixerPinConfig::SetRelativePosition
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMixerPinConfig.SetRelativePosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig::SetRelativePosition


## -description



The <code>SetRelativePosition</code> method sets the position of the stream in the display window.




## -parameters




### -param dwLeft [in]

Value specifying the x-coordinate in the upper-left corner of the display window.


### -param dwTop [in]

Value specifying the y-coordinate in the upper-left corner of the display window.


### -param dwRight [in]

Value specifying the x-coordinate in the bottom-right corner of the display window.


### -param dwBottom [in]

Value specifying the y-coordinate in the bottom-right corner of the display window.


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



This method assumes window coordinates of {0, 0, 10,000, 10,000}. Therefore, if you want your video stream to be rendered in the bottom right quarter of the display window, you would call this method with the parameters {5,000, 5,000, 10,000, 10,000}.

<div class="alert"><b>Note</b>  Values greater than 10,000 are invalid and will cause an error.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/0a2bcc3e-361d-4374-9444-717287c07116">IMixerPinConfig::GetRelativePosition</a>
 

 

