---
UID: NF:mbnapi.IMbnInterface.GetPreferredProviders
title: IMbnInterface::GetPreferredProviders (mbnapi.h)
description: Gets the list of preferred providers.
helpviewer_keywords: ["GetPreferredProviders","GetPreferredProviders method [Microsoft Broadband Networks]","GetPreferredProviders method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetPreferredProviders method","IMbnInterface.GetPreferredProviders","IMbnInterface::GetPreferredProviders","mbn.imbninterface_getpreferredproviders","mbnapi/IMbnInterface::GetPreferredProviders"]
old-location: mbn\imbninterface_getpreferredproviders.htm
tech.root: mbn
ms.assetid: cbd37f0a-4245-415d-bd74-501aa4c7ade7
ms.date: 12/05/2018
ms.keywords: GetPreferredProviders, GetPreferredProviders method [Microsoft Broadband Networks], GetPreferredProviders method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetPreferredProviders method, IMbnInterface.GetPreferredProviders, IMbnInterface::GetPreferredProviders, mbn.imbninterface_getpreferredproviders, mbnapi/IMbnInterface::GetPreferredProviders
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnInterface::GetPreferredProviders
 - mbnapi/IMbnInterface::GetPreferredProviders
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
 - IMbnInterface.GetPreferredProviders
---

# IMbnInterface::GetPreferredProviders


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the list of preferred providers.

## -parameters

### -param preferredProviders [out, retval]

Pointer to an array of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structures that contains the list of preferred providers.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.   When <b>GetPreferredProviders</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The method completed successfully.  <i>preferredProviders</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband service is currently probing for the list of preferred providers.  The calling application can get notified when the data is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onpreferredproviderschange">OnPreferredProvidersChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The device requires that a PIN must be entered for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
The SIM is not inserted.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_READ_FAULT)</b></dt>
</dl>
</td>
<td width="60%">
Unable to read from the SIM or device memory.  For example, the SIM does not have preferred provider information provisioned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this operation. CDMA devices will always return this value.

</td>
</tr>
</table>

## -remarks

<b>GetPreferredProviders</b> returns the list of providers that are stored in the interface's preferred provider list.

For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for the provider list when the error condition is over. For example, if the device requires a PIN to be entered to get the provider list, then <b>GetPreferredProviders</b> will return <b>E_MBN_PIN_REQUIRED</b>. When an application enters a PIN to unlock the device, then the Mobile Broadband service will again try to get this information from the device.

When the operating system is querying the device to get the provider list after a recoverable error has occurred, <b>GetPreferredProviders</b> immediately returns <b>E_PENDING</b>. Once the new query has completed, a notification is sent to the calling application using the appropriate callback method.  For example, after a successful PIN unlock operation, the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-onentercomplete">OnEnterComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>  would be called. After recovering from a SIM card error, the  <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onreadystatechange">OnReadyStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a> would be called.

The Mobile Broadband service will update the application about the status of any new query by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onpreferredproviderschange">OnPreferredProvidersChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

In some cases, the device's preferred provider list can be updated through the network by SMS or OTA (over-the-air update). The operating system will notify the application of any change in the preferred provider list by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onpreferredproviderschange">OnPreferredProvidersChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>