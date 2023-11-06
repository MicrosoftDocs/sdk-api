---
UID: NF:msvidctl.IMSVidCtl.get_AutoSize
title: IMSVidCtl::get_AutoSize (msvidctl.h)
description: The get_AutoSize method retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_AutoSize method","IMSVidCtl.get_AutoSize","IMSVidCtl::get_AutoSize","IMSVidCtlget_AutoSize","get_AutoSize","get_AutoSize method [Microsoft TV Technologies]","get_AutoSize method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_autosize","msvidctl/IMSVidCtl::get_AutoSize"]
old-location: mstv\imsvidctl_get_autosize.htm
tech.root: mstv
ms.assetid: 8adbc701-fd05-4520-8f06-95bd67a08d1e
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_AutoSize method, IMSVidCtl.get_AutoSize, IMSVidCtl::get_AutoSize, IMSVidCtlget_AutoSize, get_AutoSize, get_AutoSize method [Microsoft TV Technologies], get_AutoSize method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_autosize, msvidctl/IMSVidCtl::get_AutoSize
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
 - IMSVidCtl::get_AutoSize
 - msvidctl/IMSVidCtl::get_AutoSize
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
 - IMSVidCtl.get_AutoSize
---

# IMSVidCtl::get_AutoSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AutoSize</b> method retrieves a value that determines whether the Video Control is automatically resized to display its entire contents.

## -parameters

### -param pbool [out]

Pointer to a variable of type <b>VARIANT_BOOL</b> that receives the current value of the property.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_autosize">IMSVidCtl::put_AutoSize</a>