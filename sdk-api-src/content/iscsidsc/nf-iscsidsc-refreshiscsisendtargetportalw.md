---
UID: NF:iscsidsc.RefreshIScsiSendTargetPortalW
title: RefreshIScsiSendTargetPortalW function (iscsidsc.h)
description: RefreshIscsiSendTargetPortal function instructs the iSCSI initiator service to establish a discovery session with the indicated target portal and transmit a SendTargets request to refresh the list of discovered targets for the iSCSI initiator service. (Unicode)
helpviewer_keywords: ["RefreshIScsiSendTargetPortalW", "RefreshIscsiSendTargetPortal", "RefreshIscsiSendTargetPortal function [iSCSI Discovery Library API]", "RefreshIscsiSendTargetPortalW", "iscsidisc.refreshiscsisendtargetportal", "iscsidsc/RefreshIscsiSendTargetPortal", "iscsidsc/RefreshIscsiSendTargetPortalW"]
old-location: iscsidisc\refreshiscsisendtargetportal.htm
tech.root: iSCSIDisc
ms.assetid: 0e7d4e37-5d6e-4471-9cda-b9690fddf767
ms.date: 12/05/2018
ms.keywords: RefreshIScsiSendTargetPortalW, RefreshIscsiSendTargetPortal, RefreshIscsiSendTargetPortal function [iSCSI Discovery Library API], RefreshIscsiSendTargetPortalA, RefreshIscsiSendTargetPortalW, iscsidisc.refreshiscsisendtargetportal, iscsidsc/RefreshIscsiSendTargetPortal, iscsidsc/RefreshIscsiSendTargetPortalA, iscsidsc/RefreshIscsiSendTargetPortalW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RefreshIscsiSendTargetPortalW (Unicode) and RefreshIscsiSendTargetPortalA (ANSI)
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
 - RefreshIScsiSendTargetPortalW
 - iscsidsc/RefreshIScsiSendTargetPortalW
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
 - RefreshIscsiSendTargetPortal
 - RefreshIscsiSendTargetPortalA
 - RefreshIscsiSendTargetPortalW
---

# RefreshIScsiSendTargetPortalW function


## -description

The <b>RefreshIscsiSendTargetPortal</b> function instructs the iSCSI initiator service to establish a discovery session with the indicated target portal and transmit a <b>SendTargets</b> request to refresh the list of discovered targets for the iSCSI initiator service.

## -parameters

### -param InitiatorInstance [in, optional]

The name of the Host Bus Adapter (HBA) to use for the <b>SendTargets</b> request. If <b>null</b>, the iSCSI initiator service uses any HBA that can reach the indicated target portal is chosen.

### -param InitiatorPortNumber [in]

The port number on the HBA to use for the <b>SendTargets</b> request. If the value is <b>ISCSI_ALL_INITIATOR_PORTS</b>, the initiator HBA will choose the appropriate port based upon current routing information.

### -param Portal [in]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>  indicating the portal to which the iSCSI initiator service sends the <b>SendTargets</b> request to refresh the list of targets.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RefreshIScsiSendTargetPortal as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
