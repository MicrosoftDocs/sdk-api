---
UID: NF:msvidctl.IMSVidCtl.put_InputActive
title: IMSVidCtl::put_InputActive (msvidctl.h)
description: The put_InputActive method specifies the input device to use in the filter graph.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_InputActive method","IMSVidCtl.put_InputActive","IMSVidCtl::put_InputActive","IMSVidCtlput_InputActive","mstv.imsvidctl_put_inputactive","msvidctl/IMSVidCtl::put_InputActive","put_InputActive","put_InputActive method [Microsoft TV Technologies]","put_InputActive method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_inputactive.htm
tech.root: mstv
ms.assetid: 696d8ece-a377-4fe8-a790-a68d1a24e65a
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_InputActive method, IMSVidCtl.put_InputActive, IMSVidCtl::put_InputActive, IMSVidCtlput_InputActive, mstv.imsvidctl_put_inputactive, msvidctl/IMSVidCtl::put_InputActive, put_InputActive, put_InputActive method [Microsoft TV Technologies], put_InputActive method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_InputActive
 - msvidctl/IMSVidCtl::put_InputActive
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
 - IMSVidCtl.put_InputActive
---

# IMSVidCtl::put_InputActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_InputActive</b> method specifies the input device to use in the filter graph.

## -parameters

### -param pVal [in]

Specifies a pointer to the input device's <a href="/previous-versions/windows/desktop/mstv/msvidinputdevice">IMSVidInputDevice</a> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the Video Control's state is not <b>STATE_UNBUILT</b>, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-decompose">IMSVidCtl::Decompose</a> to tear down the filter graph before calling this method.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_inputactive">IMSVidCtl::get_InputActive</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_state">IMSVidCtl::get_State</a>