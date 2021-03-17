---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnSetHomeProviderComplete
title: IMbnMultiCarrierEvents::OnSetHomeProviderComplete (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation.
helpviewer_keywords: ["E_FAIL","E_INVALIDARG","E_MBN_PROVIDER_NOT_VISIBLE","HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)","IMbnMultiCarrierEvents interface [Microsoft Broadband Networks]","OnSetHomeProviderComplete method","IMbnMultiCarrierEvents.OnSetHomeProviderComplete","IMbnMultiCarrierEvents::OnSetHomeProviderComplete","OnSetHomeProviderComplete","OnSetHomeProviderComplete method [Microsoft Broadband Networks]","OnSetHomeProviderComplete method [Microsoft Broadband Networks]","IMbnMultiCarrierEvents interface","S_OK","mbn.imbnmulticarrierevents_onsethomeprovidercomplete","mbnapi/IMbnMultiCarrierEvents::OnSetHomeProviderComplete"]
old-location: mbn\imbnmulticarrierevents_onsethomeprovidercomplete.htm
tech.root: mbn
ms.assetid: 6D0B5692-4D8C-45B1-B0AF-D507FD752B1F
ms.date: 12/05/2018
ms.keywords: E_FAIL, E_INVALIDARG, E_MBN_PROVIDER_NOT_VISIBLE, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnSetHomeProviderComplete method, IMbnMultiCarrierEvents.OnSetHomeProviderComplete, IMbnMultiCarrierEvents::OnSetHomeProviderComplete, OnSetHomeProviderComplete, OnSetHomeProviderComplete method [Microsoft Broadband Networks], OnSetHomeProviderComplete method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, S_OK, mbn.imbnmulticarrierevents_onsethomeprovidercomplete, mbnapi/IMbnMultiCarrierEvents::OnSetHomeProviderComplete
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
 - IMbnMultiCarrierEvents::OnSetHomeProviderComplete
 - mbnapi/IMbnMultiCarrierEvents::OnSetHomeProviderComplete
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
 - IMbnMultiCarrierEvents.OnSetHomeProviderComplete
---

# IMbnMultiCarrierEvents::OnSetHomeProviderComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation.

## -parameters

### -param mbnInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation.

### -param status [in]

A status code that indicates the outcome of <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation  was successful.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_PROVIDER_NOT_VISIBLE"></a><a id="e_mbn_provider_not_visible"></a><dl>
<dt><b>E_MBN_PROVIDER_NOT_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
The requested provider is not visible.

</td>
</tr>
<tr>
<td width="40%"><a id="E_INVALIDARG"></a><a id="e_invalidarg"></a><dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid registration mode input, the provider ID provided as input is longer than the maximum length 7 characters, or data class provided is invalid. The Mobile Broadband service will not send the request to the device when invalid arguments are provided in the input.
In manual registration mode, this indicates that the requested provider is forbidden.

</td>
</tr>
<tr>
<td width="40%"><a id="E_FAIL"></a><a id="e_fail"></a><dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed. More information is available in the network error code.

</td>
</tr>
<tr>
<td width="40%"><a id="HRESULT_FROM_WIN32_ERROR_NOT_SUPPORTED_"></a><a id="hresult_from_win32_error_not_supported_"></a><dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support multi-carrier.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -remarks

If <i>status</i> is <b>S_OK</b>, the home provider for the interface has been successfully set to the new provider by <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a>. Otherwise, the original home provider is not changed and the previous states, such as connection, packet service etc, of the interface remain unchanged.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrierevents">IMbnMultiCarrierEvents</a>