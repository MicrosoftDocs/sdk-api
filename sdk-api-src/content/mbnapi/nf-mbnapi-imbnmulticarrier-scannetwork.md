---
UID: NF:mbnapi.IMbnMultiCarrier.ScanNetwork
title: IMbnMultiCarrier::ScanNetwork (mbnapi.h)
description: Scans the network to get a list of visible providers for a multi-carrier device.
helpviewer_keywords: ["IMbnMultiCarrier interface [Microsoft Broadband Networks]","ScanNetwork method","IMbnMultiCarrier.ScanNetwork","IMbnMultiCarrier::ScanNetwork","ScanNetwork","ScanNetwork method [Microsoft Broadband Networks]","ScanNetwork method [Microsoft Broadband Networks]","IMbnMultiCarrier interface","mbn.imbnmulticarrier_scannetwork","mbnapi/IMbnMultiCarrier::ScanNetwork"]
old-location: mbn\imbnmulticarrier_scannetwork.htm
tech.root: mbn
ms.assetid: D249B5D4-B2C3-436A-B38A-041289422F12
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrier interface [Microsoft Broadband Networks],ScanNetwork method, IMbnMultiCarrier.ScanNetwork, IMbnMultiCarrier::ScanNetwork, ScanNetwork, ScanNetwork method [Microsoft Broadband Networks], ScanNetwork method [Microsoft Broadband Networks],IMbnMultiCarrier interface, mbn.imbnmulticarrier_scannetwork, mbnapi/IMbnMultiCarrier::ScanNetwork
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
 - IMbnMultiCarrier::ScanNetwork
 - mbnapi/IMbnMultiCarrier::ScanNetwork
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
 - IMbnMultiCarrier.ScanNetwork
---

# IMbnMultiCarrier::ScanNetwork


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Scans the network to get a list of visible providers for a multi-carrier device.

## -parameters

### -param requestID [out]

Pointer to the request ID set by the operating system for this request.  The asynchronous response from <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onscannetworkcomplete">OnScanNetworkComplete</a> will contain this same <i>requestID</i>.

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
The interface is invalid. Most likely because the Mobile Broadband device has been removed from the system.

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

This method initiates a network scan operation. When completed successfully, it populates the operating system's cache of visible providers and applications can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getvisibleproviders">GetVisibleProviders</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> to get a list of visible networks.

This is a time consuming operation. Therefore, applications should first call <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getvisibleproviders">GetVisibleProviders</a> and should call <b>ScanNetwork</b> only when the cached information is old.

This is an asynchronous operation and <b>ScanNetwork</b> will return immediately. If this method returns successfully (with <b>S_OK</b>),  then upon completion of the scan operation, the operating system will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onscannetworkcomplete">OnScanNetworkComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a> to notify the application of operation completion.

If the device is removed from the system before this operation is complete, there is no guarantee that the completion notification will be received by the application.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a>