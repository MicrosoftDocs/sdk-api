---
UID: NF:msvidctl.IMSVidCtl.get_InputsAvailable
title: IMSVidCtl::get_InputsAvailable (msvidctl.h)
description: The get_InputsAvailable method retrieves the input devices that are available within a specified category.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_InputsAvailable method","IMSVidCtl.get_InputsAvailable","IMSVidCtl::get_InputsAvailable","IMSVidCtlget_InputsAvailable","get_InputsAvailable","get_InputsAvailable method [Microsoft TV Technologies]","get_InputsAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_inputsavailable","msvidctl/IMSVidCtl::get_InputsAvailable"]
old-location: mstv\imsvidctl_get_inputsavailable.htm
tech.root: mstv
ms.assetid: 7ed22c3e-745a-4680-a5fc-accef56ab348
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_InputsAvailable method, IMSVidCtl.get_InputsAvailable, IMSVidCtl::get_InputsAvailable, IMSVidCtlget_InputsAvailable, get_InputsAvailable, get_InputsAvailable method [Microsoft TV Technologies], get_InputsAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_inputsavailable, msvidctl/IMSVidCtl::get_InputsAvailable
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
 - IMSVidCtl::get_InputsAvailable
 - msvidctl/IMSVidCtl::get_InputsAvailable
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
 - IMSVidCtl.get_InputsAvailable
---

# IMSVidCtl::get_InputsAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_InputsAvailable</b> method retrieves the input devices that are available within a specified category.

## -parameters

### -param CategoryGuid [in]

<b>BSTR</b> that specifies the GUID of the category to enumerate.

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is provided for Automation clients. C++ applications can use the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get__inputsavailable">IMSVidCtl::get__InputsAvailable</a> method, which takes a GUID rather than a <b>BSTR</b> value.

If the method succeeds, the <a href="/previous-versions/windows/desktop/mstv/msvidinputdevices">IMSVidInputDevices</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>