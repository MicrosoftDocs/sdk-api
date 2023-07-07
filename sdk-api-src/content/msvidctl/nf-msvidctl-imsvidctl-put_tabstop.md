---
UID: NF:msvidctl.IMSVidCtl.put_TabStop
title: IMSVidCtl::put_TabStop (msvidctl.h)
description: The put_TabStop method specifies whether a user can use the TAB key to give the focus to the Video Control.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_TabStop method","IMSVidCtl.put_TabStop","IMSVidCtl::put_TabStop","IMSVidCtlput_TabStop","mstv.imsvidctl_put_tabstop","msvidctl/IMSVidCtl::put_TabStop","put_TabStop","put_TabStop method [Microsoft TV Technologies]","put_TabStop method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_tabstop.htm
tech.root: mstv
ms.assetid: c0e3d216-ea3f-4db4-80fd-aaf4d520ba1a
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_TabStop method, IMSVidCtl.put_TabStop, IMSVidCtl::put_TabStop, IMSVidCtlput_TabStop, mstv.imsvidctl_put_tabstop, msvidctl/IMSVidCtl::put_TabStop, put_TabStop, put_TabStop method [Microsoft TV Technologies], put_TabStop method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_TabStop
 - msvidctl/IMSVidCtl::put_TabStop
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
 - IMSVidCtl.put_TabStop
---

# IMSVidCtl::put_TabStop


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_TabStop</b> method specifies whether a user can use the TAB key to give the focus to the Video Control.

## -parameters

### -param vbool [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Include the Video Control in the tabbing order.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Do not include the Video Control in the tabbing order.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_tabstop">IMSVidCtl::get_TabStop</a>