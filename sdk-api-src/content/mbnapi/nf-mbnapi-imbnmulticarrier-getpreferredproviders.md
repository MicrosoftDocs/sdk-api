---
UID: NF:mbnapi.IMbnMultiCarrier.GetPreferredProviders
title: IMbnMultiCarrier::GetPreferredProviders
author: windows-sdk-content
description: Gets the list of subscribed providers visible in the current area for a multi-carrier device minus the current registered provider.
old-location: mbn\imbnmulticarrier_getpreferredproviders.htm
old-project: mbn
ms.assetid: 91D27D4D-5838-4D6D-BECF-B336B9F3B52A
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetPreferredProviders, GetPreferredProviders method [Microsoft Broadband Networks], GetPreferredProviders method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetPreferredProviders method, IMbnMultiCarrier.GetPreferredProviders, IMbnMultiCarrier::GetPreferredProviders, mbn.imbnmulticarrier_getpreferredproviders, mbnapi/IMbnMultiCarrier::GetPreferredProviders
ms.prod: windows
ms.technology: windows-sdk
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
 - IMbnMultiCarrier.GetPreferredProviders
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnMultiCarrier::GetPreferredProviders


## -description


Gets the list of subscribed providers visible in the current area for a multi-carrier device minus the current registered provider.


## -parameters




### -param preferredMulticarrierProviders






#### - preferredMultiCarrierProviders [out, retval]

Pointer to an array of <a href="https://msdn.microsoft.com/9D681192-1E40-4314-8E7F-8934AA8162D3">MBN_PROVIDER2</a> structures that contain the list of preferred providers. If this method returns any value other than <b>S_OK</b>, <i>preferredMultiCarrierProviders</i> is <b>NULL</b>. When <b>GetPreferredProviders</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>.


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
The method completed successfully. <i>preferredMultiCarrierProviders</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available. The Mobile Broadband service is currently probing for the list of preferred providers. The calling application can get notified when the data is available by registering for the <a href="https://msdn.microsoft.com/B2E7C42B-32B0-47D1-AA88-8A22B379B500">OnPreferredProvidersChange</a> method of <a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>.

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
Unable to read from the SIM or device memory. For example, the SIM does not have preferred provider information provisioned.

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



<b>GetPreferredProviders</b> returns the list of providers that are stored in the interface's preferred provider list.

For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for the provider list when the error condition is over. For example, if the device requires a PIN to be entered to get the provider list, then <b>GetPreferredProviders</b> will return <b>E_MBN_PIN_REQUIRED</b>. When an application enters a PIN to unlock the device, the Mobile Broadband service will again try to get this information from the device.

When Windows is querying the device to get the provider list after a recoverable error has occurred, <b>GetPreferredProviders</b> immediately returns <b>E_PENDING</b>. Once the new query has completed, a notification is sent to the calling application using the appropriate callback method. For example, after a successful PIN unlock operation, the <a href="https://msdn.microsoft.com/6a4bc731-e498-4afb-a648-0b49d2f592ca">OnEnterComplete</a> method of <a href="https://msdn.microsoft.com/4bdaa4e5-880e-4d1f-aec1-36811a0f21c1">IMbnPinEvents</a> would be called.

The Mobile Broadband service will update the application about the status of any new query by calling the <a href="https://msdn.microsoft.com/B2E7C42B-32B0-47D1-AA88-8A22B379B500">OnPreferredProvidersChange</a> method of <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>.

In some cases, the device's preferred provider list can be updated through the network by SMS or OTA (over-the-air update). Windows will notify the application of any change in the preferred provider list by calling the <a href="https://msdn.microsoft.com/B2E7C42B-32B0-47D1-AA88-8A22B379B500">OnPreferredProvidersChange</a> method of <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>.

A preferred list of providers is available if the user has multiple subscriptions (at least more than one) or the device has pre-provisioned for preferred networks and is in the coverage area of any of the networks.  This list may be empty even if the user has subscribed to multiple networks and is outside of those coverage areas.   This list will contain all of the currently visible networks that the user has subscribed to or the device has pre-provisioned for except for the currently registered network.

Provisioning can also result in a new home provider being added to the existing preferred list on a multi-carrier device. This is accomplished using <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a>.




## -see-also




<a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>
 

 

