---
UID: NF:mbnapi.IMbnMultiCarrierEvents.OnScanNetworkComplete
title: IMbnMultiCarrierEvents::OnScanNetworkComplete
author: windows-sdk-content
description: This notification method is called by the Mobile Broadband service to indicate the completion of a ScanNetwork operation.
old-location: mbn\imbnmulticarrierevents_onscannetworkcomplete.htm
tech.root: mbn
ms.assetid: EF1A39DB-351F-4105-BE56-C59477A67EC6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: E_MBN_ALREADY_ACTIVE, E_MBN_DEVICE_BUSY, E_MBN_RADIO_POWER_OFF, HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED), IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],OnScanNetworkComplete method, IMbnMultiCarrierEvents.OnScanNetworkComplete, IMbnMultiCarrierEvents::OnScanNetworkComplete, OnScanNetworkComplete, OnScanNetworkComplete method [Microsoft Broadband Networks], OnScanNetworkComplete method [Microsoft Broadband Networks],IMbnMultiCarrierEvents interface, S_OK, mbn.imbnmulticarrierevents_onscannetworkcomplete, mbnapi/IMbnMultiCarrierEvents::OnScanNetworkComplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrierEvents.OnScanNetworkComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnMultiCarrierEvents::OnScanNetworkComplete


## -description


This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a> operation.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> object that represents the Mobile Broadband device <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a> operation.


### -param requestID [in]

The request ID assigned by the Mobile Broadband service to the <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a> operation.


### -param status [in]

A status code that indicates the outcome of <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a>.

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
<td width="40%"><a id="E_MBN_RADIO_POWER_OFF"></a><a id="e_mbn_radio_power_off"></a><dl>
<dt><b>E_MBN_RADIO_POWER_OFF</b></dt>
</dl>
</td>
<td width="60%">
Can't get a visible network list because the device radio is off.  The application can issue a network scan request when it gets the radio-turned-on notification.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_DEVICE_BUSY"></a><a id="e_mbn_device_busy"></a><dl>
<dt><b>E_MBN_DEVICE_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The device is busy and can't currently perform a network scan operation.  This is returned by devices which don't support a network scan operation when it has a data connection established.

</td>
</tr>
<tr>
<td width="40%"><a id="E_MBN_ALREADY_ACTIVE"></a><a id="e_mbn_already_active"></a><dl>
<dt><b>E_MBN_ALREADY_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
A network scan operation is already in progress.

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



If <i>status</i> is <b>S_OK</b>, the Mobile Broadband service successfully updated the cached list of visible providers. An application can then call the <a href="https://msdn.microsoft.com/AC11D275-C6E3-48EE-B3DA-C9BC8648D49D">GetVisibleProviders</a> method of the passed <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> to get the list of visible providers.

If multiple applications registered for notifications, then this method will be called on all registered applications. This means that an application that did not initiate the update operation will receive a notification.




## -see-also




<a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>
 

 

