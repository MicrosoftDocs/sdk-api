---
UID: NF:msvidctl.IMSVidCtl.get_InputActive
title: IMSVidCtl::get_InputActive (msvidctl.h)
description: The get_InputActive method retrieves the input device that is currently active.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_InputActive method","IMSVidCtl.get_InputActive","IMSVidCtl::get_InputActive","IMSVidCtlget_InputActive","get_InputActive","get_InputActive method [Microsoft TV Technologies]","get_InputActive method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_inputactive","msvidctl/IMSVidCtl::get_InputActive"]
old-location: mstv\imsvidctl_get_inputactive.htm
tech.root: mstv
ms.assetid: 3451002b-5339-4b43-aefd-d66c48f7ae57
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_InputActive method, IMSVidCtl.get_InputActive, IMSVidCtl::get_InputActive, IMSVidCtlget_InputActive, get_InputActive, get_InputActive method [Microsoft TV Technologies], get_InputActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_inputactive, msvidctl/IMSVidCtl::get_InputActive
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
 - IMSVidCtl::get_InputActive
 - msvidctl/IMSVidCtl::get_InputActive
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
 - IMSVidCtl.get_InputActive
---

# IMSVidCtl::get_InputActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InputActive</b> method retrieves the input device that is currently active.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_inputactive">IMSVidCtl::put_InputActive</a>