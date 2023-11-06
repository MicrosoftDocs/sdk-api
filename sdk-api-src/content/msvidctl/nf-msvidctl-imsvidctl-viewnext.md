---
UID: NF:msvidctl.IMSVidCtl.ViewNext
title: IMSVidCtl::ViewNext (msvidctl.h)
description: The ViewNext method finds another input device to view the specified tune request.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","ViewNext method","IMSVidCtl.ViewNext","IMSVidCtl::ViewNext","IMSVidCtlViewNext","ViewNext","ViewNext method [Microsoft TV Technologies]","ViewNext method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_viewnext","msvidctl/IMSVidCtl::ViewNext"]
old-location: mstv\imsvidctl_viewnext.htm
tech.root: mstv
ms.assetid: 23b83339-f712-4b49-91f9-d0a1b02d64af
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],ViewNext method, IMSVidCtl.ViewNext, IMSVidCtl::ViewNext, IMSVidCtlViewNext, ViewNext, ViewNext method [Microsoft TV Technologies], ViewNext method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_viewnext, msvidctl/IMSVidCtl::ViewNext
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
 - IMSVidCtl::ViewNext
 - msvidctl/IMSVidCtl::ViewNext
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
 - IMSVidCtl.ViewNext
---

# IMSVidCtl::ViewNext


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ViewNext</b> method finds another input device to view the specified tune request.

This method is supported only for analog tuner devices. It does not work with digital tuners.

## -parameters

### -param v [in]

Specifies the tune request as a <b>VARIANT</b> type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method works like the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method, with the following difference: If the system has more than one tuner that supports the specified network type, the <b>ViewNext</b> method skips the current input device and uses the next one. (The ordering of devices is arbitrary.)

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a>