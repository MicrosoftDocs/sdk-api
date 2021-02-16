---
UID: NF:mbnapi.IMbnMultiCarrier.SetHomeProvider
title: IMbnMultiCarrier::SetHomeProvider (mbnapi.h)
description: Updates the home provider for a multi-carrier device.
helpviewer_keywords: ["IMbnMultiCarrier interface [Microsoft Broadband Networks]","SetHomeProvider method","IMbnMultiCarrier.SetHomeProvider","IMbnMultiCarrier::SetHomeProvider","SetHomeProvider","SetHomeProvider method [Microsoft Broadband Networks]","SetHomeProvider method [Microsoft Broadband Networks]","IMbnMultiCarrier interface","mbn.imbnmulticarrier_sethomeprovider","mbnapi/IMbnMultiCarrier::SetHomeProvider"]
old-location: mbn\imbnmulticarrier_sethomeprovider.htm
tech.root: mbn
ms.assetid: 9FDC1B01-4768-4621-9B0E-6EC9AB4275A9
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrier interface [Microsoft Broadband Networks],SetHomeProvider method, IMbnMultiCarrier.SetHomeProvider, IMbnMultiCarrier::SetHomeProvider, SetHomeProvider, SetHomeProvider method [Microsoft Broadband Networks], SetHomeProvider method [Microsoft Broadband Networks],IMbnMultiCarrier interface, mbn.imbnmulticarrier_sethomeprovider, mbnapi/IMbnMultiCarrier::SetHomeProvider
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
 - IMbnMultiCarrier::SetHomeProvider
 - mbnapi/IMbnMultiCarrier::SetHomeProvider
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
 - IMbnMultiCarrier.SetHomeProvider
---

# IMbnMultiCarrier::SetHomeProvider


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Updates the home provider for a multi-carrier device.

## -parameters

### -param homeProvider [in]

An <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider2">MBN_PROVIDER2</a> structure that contains the home provider.

<div class="alert"><b>Note</b>  <p class="note">The  <b>SignalStrength</b> and <b>SignalError</b> members must be 0.

</div>
<div> </div>

### -param requestID [out]

A pointer to the request ID set by the operating system for this request.  The asynchronous response from <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onsethomeprovidercomplete">OnSetHomeProviderComplete</a> will contain this same <i>requestID</i>.

Pointer to the request ID set by the operating system for this request. The asynchronous response will contain this same requestID.

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
Invalid interface.  The Mobile Broadband device has probably been removed from the system.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support multi-carrier.

</td>
</tr>
</table>

## -remarks

The <b>SetHomeProvider</b> method initiates an update of the home provider for the interface. This is an asynchronous operation, and the method call returns immediately. If this method returns successfully with <b>S_OK</b>, then Windows will notify the calling application about the completion status of this operation by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onsethomeprovidercomplete">OnSetHomeProviderComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a>.

The device will then automatically come up registered to the new network and indicate a registration state change. The device will continue to come up registered to this new home network across Windows reboots unless <b>SetHomeProvider</b> is used again to set a new home provider.

If the device is removed from the system before this operation is complete, there is no guarantee that the completion notification will be received by the calling application.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a>