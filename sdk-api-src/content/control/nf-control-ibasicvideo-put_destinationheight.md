---
UID: NF:control.IBasicVideo.put_DestinationHeight
title: IBasicVideo::put_DestinationHeight
author: windows-sdk-content
description: The put_DestinationHeight method sets the height of the destination rectangle.
old-location: dshow\ibasicvideo_put_destinationheight.htm
tech.root: DirectShow
ms.assetid: e530bf39-d352-4808-9ac6-5e3d322e1905
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IBasicVideo interface [DirectShow],put_DestinationHeight method, IBasicVideo.put_DestinationHeight, IBasicVideo::put_DestinationHeight, IBasicVideoput_DestinationHeight, control/IBasicVideo::put_DestinationHeight, dshow.ibasicvideo_put_destinationheight, put_DestinationHeight, put_DestinationHeight method [DirectShow], put_DestinationHeight method [DirectShow],IBasicVideo interface
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
 - IBasicVideo.put_DestinationHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicVideo::put_DestinationHeight


## -description



The <code>put_DestinationHeight</code> method sets the height of the destination rectangle.




## -parameters




### -param DestinationHeight [in]

Specifies the height, in pixels.


## -returns



Returns an <code>HRESULT</code> value. Possible values include the following.

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
Invalid argument. <i>DestinationHeight</i> must be larger than zero.

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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

