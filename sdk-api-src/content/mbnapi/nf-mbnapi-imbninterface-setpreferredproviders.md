---
UID: NF:mbnapi.IMbnInterface.SetPreferredProviders
title: IMbnInterface::SetPreferredProviders (mbnapi.h)
description: Updates the preferred providers list for the device.
helpviewer_keywords: ["IMbnInterface interface [Microsoft Broadband Networks]","SetPreferredProviders method","IMbnInterface.SetPreferredProviders","IMbnInterface::SetPreferredProviders","SetPreferredProviders","SetPreferredProviders method [Microsoft Broadband Networks]","SetPreferredProviders method [Microsoft Broadband Networks]","IMbnInterface interface","mbn.imbninterface_setpreferredproviders","mbnapi/IMbnInterface::SetPreferredProviders"]
old-location: mbn\imbninterface_setpreferredproviders.htm
tech.root: mbn
ms.assetid: 2ea95b4a-07d9-40d6-bb82-091b49c965c4
ms.date: 12/05/2018
ms.keywords: IMbnInterface interface [Microsoft Broadband Networks],SetPreferredProviders method, IMbnInterface.SetPreferredProviders, IMbnInterface::SetPreferredProviders, SetPreferredProviders, SetPreferredProviders method [Microsoft Broadband Networks], SetPreferredProviders method [Microsoft Broadband Networks],IMbnInterface interface, mbn.imbninterface_setpreferredproviders, mbnapi/IMbnInterface::SetPreferredProviders
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
 - IMbnInterface::SetPreferredProviders
 - mbnapi/IMbnInterface::SetPreferredProviders
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
 - IMbnInterface.SetPreferredProviders
---

# IMbnInterface::SetPreferredProviders


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Updates the preferred providers list for the device.

## -parameters

### -param preferredProviders [in]

An array of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structures that contains the list of preferred providers.

### -param requestID [out]

Pointer to the request ID set by the operating system for this request.  The asynchronous response will contain this same <i>requestID</i>.

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
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
</table>

## -remarks

The <b>SetPreferredProviders</b> method initiates an update of the preferred provider list for the interface. This is an asynchronous operation, and the method call returns immediately. If this method returns successfully (with <b>S_OK</b>), then the operating system will notify the calling application about the completion status of this operation by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onsetpreferredproviderscomplete">OnSetPreferredProvidersComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.


If the device is removed from the system before this operation is complete, then there is no guarantee that the completion notification will be received by the calling application.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>