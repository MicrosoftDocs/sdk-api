---
UID: NF:msvidctl.IMSVidCtl.get_OutputsAvailable
title: IMSVidCtl::get_OutputsAvailable (msvidctl.h)
description: The get_OutputsAvailable method retrieves the output devices that are available in a specified category.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_OutputsAvailable method","IMSVidCtl.get_OutputsAvailable","IMSVidCtl::get_OutputsAvailable","IMSVidCtlget_OutputsAvailable","get_OutputsAvailable","get_OutputsAvailable method [Microsoft TV Technologies]","get_OutputsAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_outputsavailable","msvidctl/IMSVidCtl::get_OutputsAvailable"]
old-location: mstv\imsvidctl_get_outputsavailable.htm
tech.root: mstv
ms.assetid: f45b752c-6b7f-4803-93fe-92ec44cd9509
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_OutputsAvailable method, IMSVidCtl.get_OutputsAvailable, IMSVidCtl::get_OutputsAvailable, IMSVidCtlget_OutputsAvailable, get_OutputsAvailable, get_OutputsAvailable method [Microsoft TV Technologies], get_OutputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_outputsavailable, msvidctl/IMSVidCtl::get_OutputsAvailable
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
 - IMSVidCtl::get_OutputsAvailable
 - msvidctl/IMSVidCtl::get_OutputsAvailable
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
 - IMSVidCtl.get_OutputsAvailable
---

# IMSVidCtl::get_OutputsAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_OutputsAvailable</b> method retrieves the output devices that are available in a specified category.

## -parameters

### -param CategoryGuid [in]

<b>BSTR</b> that specifies the GUID of the category to enumerate

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorenderersavailable">IMSVidCtl::get_AudioRenderersAvailable</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorenderersavailable">IMSVidCtl::get_VideoRenderersAvailable</a>