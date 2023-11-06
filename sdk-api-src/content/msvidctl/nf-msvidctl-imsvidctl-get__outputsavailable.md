---
UID: NF:msvidctl.IMSVidCtl.get__OutputsAvailable
title: IMSVidCtl::get__OutputsAvailable (msvidctl.h)
description: The get__OutputsAvailable method retrieves the output devices that are available in a specified category.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get__OutputsAvailable method","IMSVidCtl.get__OutputsAvailable","IMSVidCtl::get__OutputsAvailable","IMSVidCtlget__OutputsAvailable","get__OutputsAvailable","get__OutputsAvailable method [Microsoft TV Technologies]","get__OutputsAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get__outputsavailable","msvidctl/IMSVidCtl::get__OutputsAvailable"]
old-location: mstv\imsvidctl_get__outputsavailable.htm
tech.root: mstv
ms.assetid: 8242712a-9112-456b-b76d-1f382c9b637f
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get__OutputsAvailable method, IMSVidCtl.get__OutputsAvailable, IMSVidCtl::get__OutputsAvailable, IMSVidCtlget__OutputsAvailable, get__OutputsAvailable, get__OutputsAvailable method [Microsoft TV Technologies], get__OutputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get__outputsavailable, msvidctl/IMSVidCtl::get__OutputsAvailable
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
 - IMSVidCtl::get__OutputsAvailable
 - msvidctl/IMSVidCtl::get__OutputsAvailable
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
 - IMSVidCtl.get__OutputsAvailable
---

# IMSVidCtl::get__OutputsAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__OutputsAvailable</b> method retrieves the output devices that are available in a specified category.

This method is currently not supported.

## -parameters

### -param CategoryGuid [in]

Pointer to a GUID that specifies the category to enumerate.

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

To obtain the available renderers, use the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_audiorenderersavailable">get_AudioRenderersAvailable</a> and <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_videorenderersavailable">get_VideoRenderersAvailable</a> methods.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>