---
UID: NF:mbnapi.IMbnInterface.GetInterfaceCapability
title: IMbnInterface::GetInterfaceCapability (mbnapi.h)
description: Gets the capabilities of the device.
helpviewer_keywords: ["GetInterfaceCapability","GetInterfaceCapability method [Microsoft Broadband Networks]","GetInterfaceCapability method [Microsoft Broadband Networks]","IMbnInterface interface","IMbnInterface interface [Microsoft Broadband Networks]","GetInterfaceCapability method","IMbnInterface.GetInterfaceCapability","IMbnInterface::GetInterfaceCapability","mbn.imbninterface_getinterfacecapability","mbnapi/IMbnInterface::GetInterfaceCapability"]
old-location: mbn\imbninterface_getinterfacecapability.htm
tech.root: mbn
ms.assetid: cfe8f638-ad17-4118-9c79-b7ebc81c726a
ms.date: 12/05/2018
ms.keywords: GetInterfaceCapability, GetInterfaceCapability method [Microsoft Broadband Networks], GetInterfaceCapability method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetInterfaceCapability method, IMbnInterface.GetInterfaceCapability, IMbnInterface::GetInterfaceCapability, mbn.imbninterface_getinterfacecapability, mbnapi/IMbnInterface::GetInterfaceCapability
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
 - IMbnInterface::GetInterfaceCapability
 - mbnapi/IMbnInterface::GetInterfaceCapability
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
 - IMbnInterface.GetInterfaceCapability
---

# IMbnInterface::GetInterfaceCapability


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the capabilities of the device.

## -parameters

### -param interfaceCaps [out, retval]

A pointer to an <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a> structure that contains the interface capabilities.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.

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
The method completed successfully.  <i>interfaceCaps</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for the device capabilities.  The calling application can get notified when the device capabilities are available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-oninterfacecapabilityavailable">OnInterfaceCapabilityAvailable</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>

## -remarks

The <b>GetInterfaceCapability</b> method returns the interface capabilities, including the cellular technology type, the type of support for voice calls, the type of SIM used, the frequency bands supported, and the availability of SMS support. It also returns the device manufacturer name, model, and firmware name, though these are optional and may not be filled for some of the devices. For more information, see <a href="/windows/desktop/api/mbnapi/ns-mbnapi-mbn_interface_caps">MBN_INTERFACE_CAPS</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>