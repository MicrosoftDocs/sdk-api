---
UID: NF:mbnapi.IMbnConnectionContext.GetProvisionedContexts
title: IMbnConnectionContext::GetProvisionedContexts (mbnapi.h)
description: Gets a list of connection contexts.
helpviewer_keywords: ["GetProvisionedContexts","GetProvisionedContexts method [Microsoft Broadband Networks]","GetProvisionedContexts method [Microsoft Broadband Networks]","IMbnConnectionContext interface","IMbnConnectionContext interface [Microsoft Broadband Networks]","GetProvisionedContexts method","IMbnConnectionContext.GetProvisionedContexts","IMbnConnectionContext::GetProvisionedContexts","mbn.imbnconnectioncontext_getprovisionedcontexts","mbnapi/IMbnConnectionContext::GetProvisionedContexts"]
old-location: mbn\imbnconnectioncontext_getprovisionedcontexts.htm
tech.root: mbn
ms.assetid: eceba2a8-baff-436f-b561-d9e130df5702
ms.date: 12/05/2018
ms.keywords: GetProvisionedContexts, GetProvisionedContexts method [Microsoft Broadband Networks], GetProvisionedContexts method [Microsoft Broadband Networks],IMbnConnectionContext interface, IMbnConnectionContext interface [Microsoft Broadband Networks],GetProvisionedContexts method, IMbnConnectionContext.GetProvisionedContexts, IMbnConnectionContext::GetProvisionedContexts, mbn.imbnconnectioncontext_getprovisionedcontexts, mbnapi/IMbnConnectionContext::GetProvisionedContexts
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
 - IMbnConnectionContext::GetProvisionedContexts
 - mbnapi/IMbnConnectionContext::GetProvisionedContexts
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
 - IMbnConnectionContext.GetProvisionedContexts
---

# IMbnConnectionContext::GetProvisionedContexts


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets a list of connection contexts.

## -parameters

### -param provisionedContexts [out, retval]

A list of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_context">MBN_CONTEXT</a> values that represent connection contexts stored in the device. On error, this array is <b>NULL</b>. When successful, the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The connection contexts are not available.  The Mobile Broadband service is probing the device for the information.  The calling application can get notified when the connection contexts are available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontextevents-onprovisionedcontextlistchange">OnProvisionedContextListChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the connection contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support retrieval of provisioned contexts.

</td>
</tr>
</table>

## -remarks

A connection context is an abstraction of a specific set of network configuration parameters for setting up a virtual circuit or flow on top of the physical Mobile Broadband connection at layer 2. In GSM, it corresponds to the concept of a PDP context; in CDMA, it corresponds to a network profile.


In some cases, connection parameters are already available in device/SIM memory. This method can be used to get a list of stored connection contexts stored in device for the current home provider network.

Only contexts of type <b>MBN_CONTEXT_TYPE_INTERNET</b>  should be used for making data connections.

A device will return all of the stored contexts for the current home provider. Some of the contexts can be empty and they will be reported as <b>MBN_CONTEXT_TYPE_NONE</b>.

Sometimes, stored provisioned contexts can be updated by the network through SMS or OTA. Whenever there is a change in the device-provisioned contexts, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontextevents-onprovisionedcontextlistchange">OnProvisionedContextListChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>. An application can then use this method to get the updated list of provisioned contexts.


For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for this information when the error condition is over. For example, if the device required a PIN to be entered to retrieve the connection contexts, then it will return <b>E_MBN_PIN_REQUIRED</b>. When the application enters a PIN to unlock the device, then the service will again try to get this information from the device. The service will update the application about the status of the new query by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontextevents-onprovisionedcontextlistchange">OnProvisionedContextListChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontextevents">IMbnConnectionContextEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a>