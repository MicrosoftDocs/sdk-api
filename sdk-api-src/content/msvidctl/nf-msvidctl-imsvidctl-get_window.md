---
UID: NF:msvidctl.IMSVidCtl.get_Window
title: IMSVidCtl::get_Window (msvidctl.h)
description: The get_Window method retrieves the window associated with the Video Control.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_Window method","IMSVidCtl.get_Window","IMSVidCtl::get_Window","IMSVidCtlget_Window","get_Window","get_Window method [Microsoft TV Technologies]","get_Window method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_window","msvidctl/IMSVidCtl::get_Window"]
old-location: mstv\imsvidctl_get_window.htm
tech.root: mstv
ms.assetid: 88121bed-c626-4c1a-b415-8d162c43df9d
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_Window method, IMSVidCtl.get_Window, IMSVidCtl::get_Window, IMSVidCtlget_Window, get_Window, get_Window method [Microsoft TV Technologies], get_Window method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_window, msvidctl/IMSVidCtl::get_Window
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
 - IMSVidCtl::get_Window
 - msvidctl/IMSVidCtl::get_Window
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
 - IMSVidCtl.get_Window
---

# IMSVidCtl::get_Window


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Window</b> method retrieves the window associated with the Video Control.

## -parameters

### -param phwnd [out]

Receives a handle to the window.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>