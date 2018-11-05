---
UID: NF:control.IBasicVideo.SetDestinationPosition
title: IBasicVideo::SetDestinationPosition
author: windows-sdk-content
description: The SetDestinationPosition method sets the destination rectangle.
old-location: dshow\ibasicvideo_setdestinationposition.htm
tech.root: DirectShow
ms.assetid: e638eb33-5a7f-4ebc-910f-72566e251f17
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IBasicVideo interface [DirectShow],SetDestinationPosition method, IBasicVideo.SetDestinationPosition, IBasicVideo::SetDestinationPosition, IBasicVideoSetDestinationPosition, SetDestinationPosition, SetDestinationPosition method [DirectShow], SetDestinationPosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetDestinationPosition, dshow.ibasicvideo_setdestinationposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
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
 - IBasicVideo.SetDestinationPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicVideo::SetDestinationPosition


## -description



The <code>SetDestinationPosition</code> method sets the destination rectangle.




## -parameters




### -param Left [in]

Specifies the x-coordinate, in pixels.


### -param Top [in]

Specifies the y-coordinate, in pixels.


### -param Width [in]

Specifies the width, in pixels.


### -param Height [in]

Specifies the height, in pixels.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Invalid argument. <i>Width</i> and <i>Height</i> must be larger than zero.

</td>
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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer is not connected.

</td>
</tr>
</table>
 




## -remarks



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/718fcc07-1e37-4e37-ab99-39f629e65309">IBasicVideo::put_DestinationLeft</a>, <a href="https://msdn.microsoft.com/254fb104-c080-411d-9795-edcd4da41bdc">IBasicVideo::put_DestinationTop</a>, <a href="https://msdn.microsoft.com/4ae22194-19ca-4a20-9b4f-d9f39e346606">IBasicVideo::put_DestinationWidth</a>, and <a href="https://msdn.microsoft.com/e530bf39-d352-4808-9ac6-5e3d322e1905">IBasicVideo::put_DestinationHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

