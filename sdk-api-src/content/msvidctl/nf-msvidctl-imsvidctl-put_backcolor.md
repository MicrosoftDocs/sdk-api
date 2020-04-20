---
UID: NF:msvidctl.IMSVidCtl.put_BackColor
title: IMSVidCtl::put_BackColor (msvidctl.h)
description: The put_BackColor method specifies the background color of the Video Control.helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_BackColor method","IMSVidCtl.put_BackColor","IMSVidCtl::put_BackColor","IMSVidCtlput_BackColor","mstv.imsvidctl_put_backcolor","msvidctl/IMSVidCtl::put_BackColor","put_BackColor","put_BackColor method [Microsoft TV Technologies]","put_BackColor method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_backcolor.htm
tech.root: mstv
ms.assetid: d2812c19-2b69-46a8-98ab-7e1eee43f383
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_BackColor method, IMSVidCtl.put_BackColor, IMSVidCtl::put_BackColor, IMSVidCtlput_BackColor, mstv.imsvidctl_put_backcolor, msvidctl/IMSVidCtl::put_BackColor, put_BackColor, put_BackColor method [Microsoft TV Technologies], put_BackColor method [Microsoft TV Technologies],IMSVidCtl interface
f1_keywords:
- msvidctl/IMSVidCtl.put_BackColor
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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


```cpp

COLORREF orange = RGB(0xFF, 0x80, 0x00);
hr = pVideoControl->put_BackColor(static_cast<OLE_COLOR>(orange));

```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_backcolor">IMSVidCtl::get_BackColor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setbordercolor">IVMRWindowlessControl::SetBorderColor</a>
 

 

