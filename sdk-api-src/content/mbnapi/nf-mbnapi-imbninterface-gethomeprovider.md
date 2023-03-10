---
UID: NF:mbnapi.IMbnInterface.GetHomeProvider
title: IMbnInterface::GetHomeProvider (mbnapi.h)
description: Gets the home provider.
helpviewer_keywords: ["GetHomeProvider","GetHomeProvider method [Microsoft Broadband Networks]","GetHomeProvider method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetHomeProvider method","IMbnInterface.GetHomeProvider","IMbnInterface::GetHomeProvider","mbn.imbninterface_gethomeprovider","mbnapi/IMbnInterface::GetHomeProvider"]
old-location: mbn\imbninterface_gethomeprovider.htm
tech.root: mbn
ms.assetid: b9d29a2a-f41b-4e20-b9ff-559dd39e1015
ms.date: 12/05/2018
ms.keywords: GetHomeProvider, GetHomeProvider method [Microsoft Broadband Networks], GetHomeProvider method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetHomeProvider method, IMbnInterface.GetHomeProvider, IMbnInterface::GetHomeProvider, mbn.imbninterface_gethomeprovider, mbnapi/IMbnInterface::GetHomeProvider
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
 - IMbnInterface::GetHomeProvider
 - mbnapi/IMbnInterface::GetHomeProvider
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
 - IMbnInterface.GetHomeProvider
---

# IMbnInterface::GetHomeProvider


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the home provider.

## -parameters

### -param homeProvider [out, retval]

A pointer to an <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structure that represents the home provider.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Upon completion, the calling application must free the memory allocated to the  <b>providerID</b> and <b>providerName</b> members of <b>MBN_PROVIDER</b> by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>

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
The method completed successfully.  <i>homeProvider</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband service is currently probing to get the home provider.  The calling application can get notified when the home provider is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onhomeprovideravailable">OnHomeProviderAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

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
Unable to read from the SIM or device memory.  For example, the SIM does not have home provider information provisioned.

</td>
</tr>
</table>

## -remarks

<b>GetHomeProvider</b> returns the home provider information for the device. The <b>dataClass</b> field of returned <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_provider">MBN_PROVIDER</a> structure should be ignored.

For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for the home provider when the error condition is over. For example, if the device requires a PIN to be entered to retrieve this information, then it will return <b>E_MBN_PIN_REQUIRED</b>. When the application enters the PIN to unlock the device, then the Mobile Broadband service will again try to get this information from the device. The system will update the application about the status of new query by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onhomeprovideravailable">OnHomeProviderAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

The registered <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onhomeprovideravailable">OnHomeProviderAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a> can be either called when home provider information is available or the new query completed with error. Once this function returns success then this information will never change.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>