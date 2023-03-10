---
UID: NF:mbnapi.IMbnServiceActivation.Activate
title: IMbnServiceActivation::Activate (mbnapi.h)
description: Send the service activation request to the network.
helpviewer_keywords: ["Activate","Activate method [Microsoft Broadband Networks]","Activate method [Microsoft Broadband Networks]","IMbnServiceActivation interface","IMbnServiceActivation interface [Microsoft Broadband Networks]","Activate method","IMbnServiceActivation.Activate","IMbnServiceActivation::Activate","mbn.imbnserviceactivation_activate","mbnapi/IMbnServiceActivation::Activate"]
old-location: mbn\imbnserviceactivation_activate.htm
tech.root: mbn
ms.assetid: 3c131363-9403-4c7a-984d-6602b879c08e
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Microsoft Broadband Networks], Activate method [Microsoft Broadband Networks],IMbnServiceActivation interface, IMbnServiceActivation interface [Microsoft Broadband Networks],Activate method, IMbnServiceActivation.Activate, IMbnServiceActivation::Activate, mbn.imbnserviceactivation_activate, mbnapi/IMbnServiceActivation::Activate
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
 - IMbnServiceActivation::Activate
 - mbnapi/IMbnServiceActivation::Activate
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
 - IMbnServiceActivation.Activate
---

# IMbnServiceActivation::Activate


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Send the service activation request to the network.

## -parameters

### -param vendorSpecificData [in]

A vendor-specific array of bytes passed in a service activation operation. This data will be passed by the Mobile Broadband service in a SET OID_WWAN_SERVICE_ACTIVATION  OID request to the miniport driver.

### -param requestID [out]

The request ID for this operation.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely the Mobile Broadband device has been removed from the system.

Invalid interface.  Most likely the device has been removed from the system.

</td>
</tr>
</table>

## -remarks

The <b>Activate</b> method can be used by an application to activate cellular service. The format of data passed in this request is vendor-specific.

The <b>VendorSpecificBufferSize</b> field of the OID request would be set to the size of data in the SAFEARRAY,  <i>vendorSpecificData</i>. The contents of <i>vendorSpecificData</i> will be copied byte-by-byte in the OID request to the driver.

Refer to the Mobile Broadband Driver Model for more information about service activation operations.


This is an asynchronous operation that will return immediately. If the method returns without error,  then the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnserviceactivationevents-onactivationcomplete">OnActivationComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnserviceactivationevents">IMbnServiceActivationEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnserviceactivation">IMbnServiceActivation</a>