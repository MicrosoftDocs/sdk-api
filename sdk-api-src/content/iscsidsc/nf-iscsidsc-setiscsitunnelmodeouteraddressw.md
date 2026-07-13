---
UID: NF:iscsidsc.SetIScsiTunnelModeOuterAddressW
title: SetIScsiTunnelModeOuterAddressW function (iscsidsc.h)
description: SetIscsiTunnelModeOuterAddress function establishes the tunnel-mode outer address that the indicated initiator Host Bus Adapter (HBA) uses when communicating in IPsec tunnel mode through the specified port. (Unicode)
helpviewer_keywords: ["SetIScsiTunnelModeOuterAddressW", "SetIscsiTunnelModeOuterAddress", "SetIscsiTunnelModeOuterAddress function [iSCSI Discovery Library API]", "SetIscsiTunnelModeOuterAddressW", "iscsidisc.setiscsitunnelmodeouteraddress", "iscsidsc/SetIscsiTunnelModeOuterAddress", "iscsidsc/SetIscsiTunnelModeOuterAddressW"]
old-location: iscsidisc\setiscsitunnelmodeouteraddress.htm
tech.root: iSCSIDisc
ms.assetid: fdf84037-a546-49fd-9af4-21ea001587f3
ms.date: 12/05/2018
ms.keywords: SetIScsiTunnelModeOuterAddressW, SetIscsiTunnelModeOuterAddress, SetIscsiTunnelModeOuterAddress function [iSCSI Discovery Library API], SetIscsiTunnelModeOuterAddressA, SetIscsiTunnelModeOuterAddressW, iscsidisc.setiscsitunnelmodeouteraddress, iscsidsc/SetIscsiTunnelModeOuterAddress, iscsidsc/SetIscsiTunnelModeOuterAddressA, iscsidsc/SetIscsiTunnelModeOuterAddressW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetIscsiTunnelModeOuterAddressW (Unicode) and SetIscsiTunnelModeOuterAddressA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetIScsiTunnelModeOuterAddressW
 - iscsidsc/SetIScsiTunnelModeOuterAddressW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iscsidsc.dll
api_name:
 - SetIscsiTunnelModeOuterAddress
 - SetIscsiTunnelModeOuterAddressA
 - SetIscsiTunnelModeOuterAddressW
---

# SetIScsiTunnelModeOuterAddressW function


## -description

<b>SetIscsiTunnelModeOuterAddress</b> function establishes the tunnel-mode outer address that the indicated initiator Host Bus Adapter (HBA) uses when communicating in IPsec tunnel mode through the specified port.

## -parameters

### -param InitiatorName [in, optional]

The name of the initiator with which the tunnel-mode outer address will be associated. If this parameter is <b>null</b>, all HBA initiators are configured to use the indicated tunnel-mode outer address.

### -param InitiatorPortNumber [in]

Indicates the number of the port with which the tunnel-mode outer address is associated. If this parameter contains <b>ISCSI_ALL_PORTS</b>, all ports on the indicated initiator are associated with the tunnel-mode outer address.

### -param DestinationAddress [in]

The destination address to associate with the tunnel-mode outer address indicated by <i>OuterModeAddress</i>.

### -param OuterModeAddress [in]

The tunnel-mode outer address to associate with indicated initiators and ports.

### -param Persist [in]

When <b>true</b>, this parameter indicates that the iSCSI initiator service stores the tunnel-mode outer address in non-volatile memory and that the address will persist across restarts of the initiator and the iSCSI initiator service.

## -returns

Returns ERROR_SUCCESS if the operation succeeds.Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -remarks

> [!NOTE]
> The iscsidsc.h header defines SetIScsiTunnelModeOuterAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

