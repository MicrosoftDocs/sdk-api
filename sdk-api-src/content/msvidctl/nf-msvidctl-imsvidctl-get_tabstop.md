---
UID: NF:msvidctl.IMSVidCtl.get_TabStop
title: IMSVidCtl::get_TabStop (msvidctl.h)
description: The get_TabStop method queries whether a user can use the TAB key to give the focus to the Video Control.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_TabStop method","IMSVidCtl.get_TabStop","IMSVidCtl::get_TabStop","IMSVidCtlget_TabStop","get_TabStop","get_TabStop method [Microsoft TV Technologies]","get_TabStop method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_tabstop","msvidctl/IMSVidCtl::get_TabStop"]
old-location: mstv\imsvidctl_get_tabstop.htm
tech.root: mstv
ms.assetid: 9579144d-22b6-4d97-a52c-0d8bbc9066e4
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_TabStop method, IMSVidCtl.get_TabStop, IMSVidCtl::get_TabStop, IMSVidCtlget_TabStop, get_TabStop, get_TabStop method [Microsoft TV Technologies], get_TabStop method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_tabstop, msvidctl/IMSVidCtl::get_TabStop
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
 - IMSVidCtl::get_TabStop
 - msvidctl/IMSVidCtl::get_TabStop
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
 - IMSVidCtl.get_TabStop
---

# IMSVidCtl::get_TabStop


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_TabStop</b> method queries whether a user can use the TAB key to give the focus to the Video Control.

## -parameters

### -param pbool [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control is in the tabbing order.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control is not in the tabbing order.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_tabstop">IMSVidCtl::put_TabStop</a>