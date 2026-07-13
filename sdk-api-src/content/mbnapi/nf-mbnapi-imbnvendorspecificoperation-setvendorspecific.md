---
UID: NF:mbnapi.IMbnVendorSpecificOperation.SetVendorSpecific
title: IMbnVendorSpecificOperation::SetVendorSpecific (mbnapi.h)
description: Sends a request to the underlying Mobile Broadband device miniport driver.
helpviewer_keywords: ["IMbnVendorSpecificOperation interface [Microsoft Broadband Networks]","SetVendorSpecific method","IMbnVendorSpecificOperation.SetVendorSpecific","IMbnVendorSpecificOperation::SetVendorSpecific","SetVendorSpecific","SetVendorSpecific method [Microsoft Broadband Networks]","SetVendorSpecific method [Microsoft Broadband Networks]","IMbnVendorSpecificOperation interface","mbn.imbnvendorspecificoperation_setvendorspecific","mbnapi/IMbnVendorSpecificOperation::SetVendorSpecific"]
old-location: mbn\imbnvendorspecificoperation_setvendorspecific.htm
tech.root: mbn
ms.assetid: adae9d6c-3fd4-42f6-8f6a-0047f3e0aad0
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificOperation interface [Microsoft Broadband Networks],SetVendorSpecific method, IMbnVendorSpecificOperation.SetVendorSpecific, IMbnVendorSpecificOperation::SetVendorSpecific, SetVendorSpecific, SetVendorSpecific method [Microsoft Broadband Networks], SetVendorSpecific method [Microsoft Broadband Networks],IMbnVendorSpecificOperation interface, mbn.imbnvendorspecificoperation_setvendorspecific, mbnapi/IMbnVendorSpecificOperation::SetVendorSpecific
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnVendorSpecificOperation::SetVendorSpecific
 - mbnapi/IMbnVendorSpecificOperation::SetVendorSpecific
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnVendorSpecificOperation.SetVendorSpecific
---

# IMbnVendorSpecificOperation::SetVendorSpecific


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sends a request to the underlying Mobile Broadband device miniport driver.

## -parameters

### -param vendorSpecificData [in]

A byte array that is passed in to the miniport driver.

### -param requestID [out]

A unique request ID assigned by the Mobile Broadband service to identify this request.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SetVendorSpecific</b> exists to implement vendor-specific functionality which is not otherwise covered in the Mobile Broadband API.

The Mobile Broadband service will issue a SET OID request to the underlying miniport driver for OID_WWAN_VENDOR_SPECIFIC OID.  <i>VendorspecificData</i> will be copied byte by byte into the data buffer passed in the OID request.

This is an asynchronous operation and <b>SetVendorSpecific</b> will return immediately.  On completion of the operation, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnvendorspecificevents-onsetvendorspecificcomplete">OnSetVendorSpecificComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificevents">IMbnVendorSpecificEvents</a> interface.

Refer to  the Mobile Broadband Driver Model for more information about vendor specific operations.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificoperation">IMbnVendorSpecificOperation</a>