---
UID: NF:msvidctl.IMSVidCtl.get_BackColor
title: IMSVidCtl::get_BackColor (msvidctl.h)
description: The get_BackColor method retrieves the background color of the Video Control.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_BackColor method","IMSVidCtl.get_BackColor","IMSVidCtl::get_BackColor","IMSVidCtlget_BackColor","get_BackColor","get_BackColor method [Microsoft TV Technologies]","get_BackColor method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_backcolor","msvidctl/IMSVidCtl::get_BackColor"]
old-location: mstv\imsvidctl_get_backcolor.htm
tech.root: mstv
ms.assetid: 1f67f1f9-e4e1-47fc-a92d-b6dfb65e7ec9
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_BackColor method, IMSVidCtl.get_BackColor, IMSVidCtl::get_BackColor, IMSVidCtlget_BackColor, get_BackColor, get_BackColor method [Microsoft TV Technologies], get_BackColor method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_backcolor, msvidctl/IMSVidCtl::get_BackColor
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidCtl::get_BackColor
 - msvidctl/IMSVidCtl::get_BackColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_BackColor
---

# IMSVidCtl::get_BackColor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_BackColor</b> method retrieves the background color of the Video Control.

## -parameters

### -param backcolor [out]

Receives an <b>OLE_COLOR</b> value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_backcolor">IMSVidCtl::put_BackColor</a>