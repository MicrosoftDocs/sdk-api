---
UID: NF:mbnapi.IMbnConnectionContext.SetProvisionedContext
title: IMbnConnectionContext::SetProvisionedContext (mbnapi.h)
description: Adds or updates a provisioned context.
helpviewer_keywords: ["IMbnConnectionContext interface [Microsoft Broadband Networks]","SetProvisionedContext method","IMbnConnectionContext.SetProvisionedContext","IMbnConnectionContext::SetProvisionedContext","SetProvisionedContext","SetProvisionedContext method [Microsoft Broadband Networks]","SetProvisionedContext method [Microsoft Broadband Networks]","IMbnConnectionContext interface","mbn.imbnconnectioncontext_setprovisionedcontext","mbnapi/IMbnConnectionContext::SetProvisionedContext"]
old-location: mbn\imbnconnectioncontext_setprovisionedcontext.htm
tech.root: mbn
ms.assetid: 738a3037-01a9-465a-a67d-979a29968b68
ms.date: 12/05/2018
ms.keywords: IMbnConnectionContext interface [Microsoft Broadband Networks],SetProvisionedContext method, IMbnConnectionContext.SetProvisionedContext, IMbnConnectionContext::SetProvisionedContext, SetProvisionedContext, SetProvisionedContext method [Microsoft Broadband Networks], SetProvisionedContext method [Microsoft Broadband Networks],IMbnConnectionContext interface, mbn.imbnconnectioncontext_setprovisionedcontext, mbnapi/IMbnConnectionContext::SetProvisionedContext
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
 - IMbnConnectionContext::SetProvisionedContext
 - mbnapi/IMbnConnectionContext::SetProvisionedContext
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
 - IMbnConnectionContext.SetProvisionedContext
---

# IMbnConnectionContext::SetProvisionedContext


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Adds or updates a provisioned context.

## -parameters

### -param provisionedContexts [in]

An <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> structure that specifies the provisioned context to be stored in the device or SIM.

### -param providerID [in]

A string that represents the network provider ID for which the provisioned context should be stored.  The device should return the added provisioned context in response to any subsequent query when a SIM with this home provider ID is in the device.

### -param requestID [out]

A request ID set by the Mobile Broadband service to identify this asynchronous request.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface.  Most likely the Mobile Broadband device has been removed from the system.

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
<dt><b>E_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
<i>providerID</i>  is not valid.

</td>
</tr>
</table>

## -remarks

The <b>contextID</b> of <i>provisionedContexts</i> specifies the index in the device or SIM memory where the context is to be stored.  If it is set to <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_context_constants">MBN_CONTEXT_ID_APPEND</a>, then the device shall find the appropriate index to store the context.

This is an asynchronous operation and <b>SetProvisionedContext</b> will return immediately. When the operation is complete, the Mobile Broadband service will notify the application by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontextevents-onsetprovisionedcontextcomplete">OnSetProvisionedContextComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>.

Additions to the provisioned context list for the current home provider ID will not be available for querying until the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontextevents-onprovisionedcontextlistchange">OnProvisionedContextListChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a> has been called.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a>