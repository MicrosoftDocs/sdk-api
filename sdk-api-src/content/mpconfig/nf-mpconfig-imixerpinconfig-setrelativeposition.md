---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

