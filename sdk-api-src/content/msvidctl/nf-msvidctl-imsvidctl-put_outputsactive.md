---
UID: NF:msvidctl.IMSVidCtl.put_OutputsActive
title: IMSVidCtl::put_OutputsActive (msvidctl.h)
description: The put_OutputsActive method specifies the active output devices.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_OutputsActive method","IMSVidCtl.put_OutputsActive","IMSVidCtl::put_OutputsActive","IMSVidCtlput_OutputsActive","mstv.imsvidctl_put_outputsactive","msvidctl/IMSVidCtl::put_OutputsActive","put_OutputsActive","put_OutputsActive method [Microsoft TV Technologies]","put_OutputsActive method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_outputsactive.htm
tech.root: mstv
ms.assetid: 636cedef-f6e5-40f2-8f1c-9f886d618ad0
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_OutputsActive method, IMSVidCtl.put_OutputsActive, IMSVidCtl::put_OutputsActive, IMSVidCtlput_OutputsActive, mstv.imsvidctl_put_outputsactive, msvidctl/IMSVidCtl::put_OutputsActive, put_OutputsActive, put_OutputsActive method [Microsoft TV Technologies], put_OutputsActive method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_OutputsActive
 - msvidctl/IMSVidCtl::put_OutputsActive
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
 - IMSVidCtl.put_OutputsActive
---

# IMSVidCtl::put_OutputsActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_OutputsActive</b> method specifies the active output devices.

## -parameters

### -param pVal [in]

Pointer to the new collection of output devices.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_outputsactive">IMSVidCtl::get_OutputsActive</a>