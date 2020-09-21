---
UID: NF:mbnapi.IMbnInterface.GetVisibleProviders
title: IMbnInterface::GetVisibleProviders (mbnapi.h)
description: Gets the list of visible providers.
helpviewer_keywords: ["GetVisibleProviders","GetVisibleProviders method [Microsoft Broadband Networks]","GetVisibleProviders method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetVisibleProviders method","IMbnInterface.GetVisibleProviders","IMbnInterface::GetVisibleProviders","mbn.imbninterface_getvisibleproviders","mbnapi/IMbnInterface::GetVisibleProviders"]
old-location: mbn\imbninterface_getvisibleproviders.htm
tech.root: mbn
ms.assetid: 916c29ee-adb3-402c-b4f3-97b8977f44ac
ms.date: 12/05/2018
ms.keywords: GetVisibleProviders, GetVisibleProviders method [Microsoft Broadband Networks], GetVisibleProviders method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetVisibleProviders method, IMbnInterface.GetVisibleProviders, IMbnInterface::GetVisibleProviders, mbn.imbninterface_getvisibleproviders, mbnapi/IMbnInterface::GetVisibleProviders
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
 - IMbnInterface::GetVisibleProviders
 - mbnapi/IMbnInterface::GetVisibleProviders
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
 - IMbnInterface.GetVisibleProviders
---

# IMbnInterface::GetVisibleProviders


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the list of visible providers.

## -parameters

### -param age [out, retval]

A pointer to the time in seconds since the last refresh of the visible provider list from the device.

### -param visibleProviders [out, retval]

Pointer to an array of  <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structures that contains the list of providers for the interface.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Otherwise, upon completion, the calling program must free the allocated memory  by calling <a href="/windows/win32/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The method completed successfully.  <i>visibleProviders</i> contains valid values.  Based on the age of the information, the calling application can decide to issue a new call to <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-scannetwork">ScanNetwork</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  An active network scan is in progress.  The calling application can get notified when the device capabilities are available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onscannetworkcomplete">OnScanNetworkComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Mobile Broadband's cache of the visible network list is invalid.  The calling application should call <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-scannetwork">ScanNetwork</a> to populate the cache.

</td>
</tr>
</table>

## -remarks

This method returns the list of currently visible providers.  CDMA devices will report only their home provider if any network in their preferred roaming list (PRL) is available.

To avoid frequent network scan operations, the operating system maintains a list of recent scan operations and the provider list is returned from the cached list.

An application can call this method to get a list of visible providers upon the completion of <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-scannetwork">ScanNetwork</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>