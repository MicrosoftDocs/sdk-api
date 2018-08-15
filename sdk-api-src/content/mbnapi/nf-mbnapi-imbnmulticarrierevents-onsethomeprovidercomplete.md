---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnSetHomeProviderComplete
title: IMbnMultiCarrierEvents::OnSetHomeProviderComplete
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation.
old-location: mbn\imbnmulticarrierevents_onsethomeprovidercomplete.htm
old-project: mbn
ms.assetid: 6D0B5692-4D8C-45B1-B0AF-D507FD752B1F
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: E_FAIL, E_INVALIDARG, E_MBN_PROVIDER_NOT_VISIBLE, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnSetHomeProviderComplete method, IMbnMultiCarrierEvents.OnSetHomeProviderComplete, IMbnMultiCarrierEvents::OnSetHomeProviderComplete, OnSetHomeProviderComplete, OnSetHomeProviderComplete method [Microsoft Broadband Networks], OnSetHomeProviderComplete method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, S_OK, mbn.imbnmulticarrierevents_onsethomeprovidercomplete, mbnapi/IMbnMultiCarrierEvents::OnSetHomeProviderComplete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrierEvents.OnSetHomeProviderComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnMultiCarrierEvents::OnSetHomeProviderComplete


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation.


### -param requestID [in]

The request ID assigned by the Mobile Broadband service to the <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation.


### -param status [in]

A status code that indicates the outcome of <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a>.

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



If <i>status</i> is <b>S_OK</b>, the home provider for the interface has been successfully set to the new provider by <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a>. Otherwise, the original home provider is not changed and the previous states, such as connection, packet service etc, of the interface remain unchanged.




## -see-also




<a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>
 

 

