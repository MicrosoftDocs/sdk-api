---
UID: NF:msvidctl.IMSVidCtl.get_DisplaySize
title: IMSVidCtl::get_DisplaySize (msvidctl.h)
description: The get_DisplaySize method retrieves the display size.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_DisplaySize method","IMSVidCtl.get_DisplaySize","IMSVidCtl::get_DisplaySize","IMSVidCtlget_DisplaySize","get_DisplaySize","get_DisplaySize method [Microsoft TV Technologies]","get_DisplaySize method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_displaysize","msvidctl/IMSVidCtl::get_DisplaySize"]
old-location: mstv\imsvidctl_get_displaysize.htm
tech.root: mstv
ms.assetid: f3d5ed73-4781-46fb-8df4-a7dc339b755c
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_DisplaySize method, IMSVidCtl.get_DisplaySize, IMSVidCtl::get_DisplaySize, IMSVidCtlget_DisplaySize, get_DisplaySize, get_DisplaySize method [Microsoft TV Technologies], get_DisplaySize method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_displaysize, msvidctl/IMSVidCtl::get_DisplaySize
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
 - IMSVidCtl::get_DisplaySize
 - msvidctl/IMSVidCtl::get_DisplaySize
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
 - IMSVidCtl.get_DisplaySize
---

# IMSVidCtl::get_DisplaySize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DisplaySize</b> method retrieves the display size.

## -parameters

### -param CurrentValue [out]

Receives a member of the <a href="/previous-versions/windows/desktop/api/msvidctl/ne-msvidctl-displaysizelist">DisplaySizeList</a> enumeration.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The display size has no effect if the <b>AutoSize</b> property is false.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_autosize">IMSVidCtl::get_AutoSize</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_displaysize">IMSVidCtl::put_DisplaySize</a>