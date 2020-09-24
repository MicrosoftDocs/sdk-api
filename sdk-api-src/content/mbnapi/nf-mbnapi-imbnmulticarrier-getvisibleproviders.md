---
UID: NF:mbnapi.IMbnMultiCarrier.GetVisibleProviders
title: IMbnMultiCarrier::GetVisibleProviders (mbnapi.h)
description: Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.
helpviewer_keywords: ["GetVisibleProviders","GetVisibleProviders method [Microsoft Broadband Networks]","GetVisibleProviders method [Microsoft Broadband Networks]","IMbnMultiCarrier interface","IMbnMultiCarrier interface [Microsoft Broadband Networks]","GetVisibleProviders method","IMbnMultiCarrier.GetVisibleProviders","IMbnMultiCarrier::GetVisibleProviders","mbn.imbnmulticarrier_getvisibleproviders","mbnapi/IMbnMultiCarrier::GetVisibleProviders"]
old-location: mbn\imbnmulticarrier_getvisibleproviders.htm
tech.root: mbn
ms.assetid: AC11D275-C6E3-48EE-B3DA-C9BC8648D49D
ms.date: 12/05/2018
ms.keywords: GetVisibleProviders, GetVisibleProviders method [Microsoft Broadband Networks], GetVisibleProviders method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetVisibleProviders method, IMbnMultiCarrier.GetVisibleProviders, IMbnMultiCarrier::GetVisibleProviders, mbn.imbnmulticarrier_getvisibleproviders, mbnapi/IMbnMultiCarrier::GetVisibleProviders
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
 - IMbnMultiCarrier::GetVisibleProviders
 - mbnapi/IMbnMultiCarrier::GetVisibleProviders
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
 - IMbnMultiCarrier.GetVisibleProviders
---

# IMbnMultiCarrier::GetVisibleProviders


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.

## -parameters

### -param age [out]

A pointer to the time, in seconds, since the last refresh of the visible provider list for the device.

### -param visibleProviders [out, retval]

Pointer to an array of <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider2">MBN_PROVIDER2</a> structures that contains the list of providers for the interface. If this method returns any value other than <b>S_OK</b>, <i>visibleProviders</i> is <b>NULL</b>. When <b>GetVisibleProviders</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>.

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
The method completed successfully. <i>visibleProviders</i> contains valid values. Based on the age of the information, the calling application can decide to issue a new call to <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-scannetwork">ScanNetwork</a>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available. An active network scan is in progress. The calling application can get notified when the device capabilities are available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onscannetworkcomplete">OnScanNetworkComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Mobile Broadband's cache of the visible network list is invalid. The calling application should call <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-scannetwork">ScanNetwork</a> to populate the cache.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support multi-carrier.

</td>
</tr>
</table>

## -remarks

This method returns the list of currently visible providers. CDMA devices will report only their home provider if any network in their preferred roaming list (PRL) is available.

To avoid frequent network scan operations,  Windows maintains a list of recent scan operations and the provider list is returned from the cached list.

An application can call this method to get a list of visible providers upon the completion of <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-scannetwork">ScanNetwork</a>.

This list contains all the currently visible networks available at the user’s location excluding the ones reported by current registered provider and the list of preferred providers.  This list contains network entries that users have not subscribed to.  This list providers the user with an additional set of network choices they can potentially sign up for.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a>