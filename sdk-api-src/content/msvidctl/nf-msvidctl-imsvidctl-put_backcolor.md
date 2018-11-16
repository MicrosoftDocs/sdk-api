---
UID: NF:msvidctl.IMSVidCtl.put_BackColor
title: IMSVidCtl::put_BackColor
author: windows-sdk-content
description: The put_BackColor method specifies the background color of the Video Control.
old-location: mstv\imsvidctl_put_backcolor.htm
tech.root: mstv
ms.assetid: d2812c19-2b69-46a8-98ab-7e1eee43f383
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_BackColor method, IMSVidCtl.put_BackColor, IMSVidCtl::put_BackColor, IMSVidCtlput_BackColor, mstv.imsvidctl_put_backcolor, msvidctl/IMSVidCtl::put_BackColor, put_BackColor, put_BackColor method [Microsoft TV Technologies], put_BackColor method [Microsoft TV Technologies],IMSVidCtl interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - msvidctl.h
api_name:
 - IMSVidCtl.put_BackColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msvidctl.h
: 
- IMSVidCtl.put_BackColor
: 
---

# IMSVidCtl::put_BackColor


## -description


The <b>put_BackColor</b> method specifies the background color of the Video Control.


## -parameters




### -param backcolor [in]

Specifies the background color as an <b>OLE_COLOR</b> value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The Video Control uses the background color when the filter graph is stopped or unbuilt. It also uses this color in letterbox mode to paint unused areas of the video rectangle. The background color is sometimes called the "border" color.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
COLORREF orange = RGB(0xFF, 0x80, 0x00);
hr = pVideoControl-&gt;put_BackColor(static_cast&lt;OLE_COLOR&gt;(orange));
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/1f67f1f9-e4e1-47fc-a92d-b6dfb65e7ec9">IMSVidCtl::get_BackColor</a>



<a href="https://msdn.microsoft.com/d58ce18f-ddc4-4d91-b086-8829056f4508">IVMRWindowlessControl::SetBorderColor</a>
 

 

