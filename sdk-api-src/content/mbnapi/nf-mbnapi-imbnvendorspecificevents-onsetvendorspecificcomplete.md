---
UID: NF:mbnapi.IMbnVendorSpecificEvents.OnSetVendorSpecificComplete
title: IMbnVendorSpecificEvents::OnSetVendorSpecificComplete (mbnapi.h)
description: Notification method indicating that a vendor-specific operation has completed.
helpviewer_keywords: ["IMbnVendorSpecificEvents interface [Microsoft Broadband Networks]","OnSetVendorSpecificComplete method","IMbnVendorSpecificEvents.OnSetVendorSpecificComplete","IMbnVendorSpecificEvents::OnSetVendorSpecificComplete","OnSetVendorSpecificComplete","OnSetVendorSpecificComplete method [Microsoft Broadband Networks]","OnSetVendorSpecificComplete method [Microsoft Broadband Networks]","IMbnVendorSpecificEvents interface","mbn.imbnvendorspecificevents_onsetvendorspecificcomplete","mbnapi/IMbnVendorSpecificEvents::OnSetVendorSpecificComplete"]
old-location: mbn\imbnvendorspecificevents_onsetvendorspecificcomplete.htm
tech.root: mbn
ms.assetid: fc45b203-3e8e-436c-a554-164634026ecc
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],OnSetVendorSpecificComplete method, IMbnVendorSpecificEvents.OnSetVendorSpecificComplete, IMbnVendorSpecificEvents::OnSetVendorSpecificComplete, OnSetVendorSpecificComplete, OnSetVendorSpecificComplete method [Microsoft Broadband Networks], OnSetVendorSpecificComplete method [Microsoft Broadband Networks],IMbnVendorSpecificEvents interface, mbn.imbnvendorspecificevents_onsetvendorspecificcomplete, mbnapi/IMbnVendorSpecificEvents::OnSetVendorSpecificComplete
f1_keywords:
- mbnapi/IMbnVendorSpecificEvents.OnSetVendorSpecificComplete
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnVendorSpecificEvents.OnSetVendorSpecificComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnVendorSpecificEvents::OnSetVendorSpecificComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method indicating that a vendor-specific operation has completed.


## -parameters




### -param vendorOperation [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificoperation">IMbnVendorSpecificOperation</a> interface representing the operation that completed.


### -param vendorSpecificData [in]

A byte array containing the data returned by underlying miniport driver. 


### -param requestID [in]

A request ID assigned by the Mobile Broadband service to identify the vendor-specific operation request.


## -returns



This method must return <b>S_OK</b>.




## -remarks



This byte array contains the byte by byte copy of data returned by underlying miniport driver. The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificevents">IMbnVendorSpecificEvents</a>
 

 

