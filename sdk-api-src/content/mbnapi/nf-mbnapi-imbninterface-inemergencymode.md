---
UID: NF:mbnapi.IMbnInterface.InEmergencyMode
title: IMbnInterface::InEmergencyMode (mbnapi.h)
description: Determines whether the device is in emergency mode.
helpviewer_keywords: ["IMbnInterface interface [Microsoft Broadband Networks]","InEmergencyMode method","IMbnInterface.InEmergencyMode","IMbnInterface::InEmergencyMode","InEmergencyMode","InEmergencyMode method [Microsoft Broadband Networks]","InEmergencyMode method [Microsoft Broadband Networks]","IMbnInterface interface","mbn.imbninterface_inemergencymode","mbnapi/IMbnInterface::InEmergencyMode"]
old-location: mbn\imbninterface_inemergencymode.htm
tech.root: mbn
ms.assetid: b4ce2c10-627d-4cbe-a884-7bb8731c3bcf
ms.date: 12/05/2018
ms.keywords: IMbnInterface interface [Microsoft Broadband Networks],InEmergencyMode method, IMbnInterface.InEmergencyMode, IMbnInterface::InEmergencyMode, InEmergencyMode, InEmergencyMode method [Microsoft Broadband Networks], InEmergencyMode method [Microsoft Broadband Networks],IMbnInterface interface, mbn.imbninterface_inemergencymode, mbnapi/IMbnInterface::InEmergencyMode
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
 - IMbnInterface::InEmergencyMode
 - mbnapi/IMbnInterface::InEmergencyMode
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
 - IMbnInterface.InEmergencyMode
---

# IMbnInterface::InEmergencyMode


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Determines whether the device is in emergency mode.

## -parameters

### -param emergencyMode [out]

Points to VARIANT_TRUE if the device is in emergency mode, and VARIANT_FALSE if it is not.

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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband  service is currently probing for this information.  The calling application can be notified when the data is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterfaceevents-onemergencymodechange">OnEmergencyModeChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>.

</td>
</tr>
</table>

## -remarks

If a device cannot register on the network for any reason, then the device may automatically register onto a network in emergency mode. For example, a device cannot register on the network if the SIM is not inserted, user subscription validity expired, or roaming is not enabled for user.  In emergency mode, device can be used in limited mode for voice calls to emergency numbers.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>