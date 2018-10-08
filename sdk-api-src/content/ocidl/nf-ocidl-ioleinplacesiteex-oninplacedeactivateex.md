---
UID: NF:ocidl.IOleInPlaceSiteEx.OnInPlaceDeactivateEx
title: IOleInPlaceSiteEx::OnInPlaceDeactivateEx
author: windows-sdk-content
description: Notifies the container if the object needs to be redrawn upon deactivation.
old-location: com\ioleinplacesiteex_oninplacedeactivateex.htm
tech.root: com
ms.assetid: c3c68b46-adca-4f8d-86c2-075b72f7c656
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IOleInPlaceSiteEx interface [COM],OnInPlaceDeactivateEx method, IOleInPlaceSiteEx.OnInPlaceDeactivateEx, IOleInPlaceSiteEx::OnInPlaceDeactivateEx, IOleInPlaceSiteWindowless.OnInPlaceDeactivateEx, OnInPlaceDeactivateEx, OnInPlaceDeactivateEx method [COM], OnInPlaceDeactivateEx method [COM],IOleInPlaceSiteEx interface, _ole_ioleinplacesiteex_oninplacedeactivateex, com.ioleinplacesiteex_oninplacedeactivateex, ocidl/IOleInPlaceSiteEx::OnInPlaceDeactivateEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
 - wmp.dll
api_name:
 - IOleInPlaceSiteEx.OnInPlaceDeactivateEx
 - IOleInPlaceSiteWindowless.OnInPlaceDeactivateEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceSiteEx::OnInPlaceDeactivateEx


## -description


Notifies the container if the object needs to be redrawn upon deactivation.


## -parameters




### -param fNoRedraw [in]

If <b>TRUE</b>, the container need not redraw the object after completing the deactivation; if <b>FALSE</b> the object must be redrawn after deactivation.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



This method replaces <a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">IOleInPlaceSite::OnInPlaceDeactivate</a>. If the older method is used, the object must always be redrawn on deactivation.




## -see-also




<a href="https://msdn.microsoft.com/070aac4e-94b6-4e23-b132-1dc833774c8b">IOleInPlaceSite::OnInPlaceDeactivate</a>



<a href="https://msdn.microsoft.com/d93e6d23-7867-43e4-8ab9-efe609362c18">IOleInPlaceSiteEx</a>
 

 

