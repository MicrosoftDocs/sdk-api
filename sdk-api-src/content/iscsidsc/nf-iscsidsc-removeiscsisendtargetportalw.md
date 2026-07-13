---
UID: NF:iscsidsc.RemoveIScsiSendTargetPortalW
title: RemoveIScsiSendTargetPortalW function (iscsidsc.h)
description: RemoveIscsiSendTargetPortal function removes a portal from the list of portals to which the iSCSI initiator service sends SendTargets requests for target discovery. (Unicode)
helpviewer_keywords: ["RemoveIScsiSendTargetPortalW", "RemoveIscsiSendTargetPortal", "RemoveIscsiSendTargetPortal function [iSCSI Discovery Library API]", "RemoveIscsiSendTargetPortalW", "iscsidisc.removeiscsisendtargetportal", "iscsidsc/RemoveIscsiSendTargetPortal", "iscsidsc/RemoveIscsiSendTargetPortalW"]
old-location: iscsidisc\removeiscsisendtargetportal.htm
tech.root: iSCSIDisc
ms.assetid: f9c05a86-3484-4092-b384-c599fbf1e60f
ms.date: 12/05/2018
ms.keywords: RemoveIScsiSendTargetPortalW, RemoveIscsiSendTargetPortal, RemoveIscsiSendTargetPortal function [iSCSI Discovery Library API], RemoveIscsiSendTargetPortalA, RemoveIscsiSendTargetPortalW, iscsidisc.removeiscsisendtargetportal, iscsidsc/RemoveIscsiSendTargetPortal, iscsidsc/RemoveIscsiSendTargetPortalA, iscsidsc/RemoveIscsiSendTargetPortalW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveIscsiSendTargetPortalW (Unicode) and RemoveIscsiSendTargetPortalA (ANSI)
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
 - RemoveIScsiSendTargetPortalW
 - iscsidsc/RemoveIScsiSendTargetPortalW
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
 - RemoveIscsiSendTargetPortal
 - RemoveIscsiSendTargetPortalA
 - RemoveIscsiSendTargetPortalW
---

# RemoveIScsiSendTargetPortalW function


## -description

The <b>RemoveIscsiSendTargetPortal</b> function removes a portal from the list of portals to which the iSCSI initiator service sends <b>SendTargets</b> requests for target discovery.

## -parameters

### -param InitiatorInstance [in, optional]

The name of the Host Bus Adapter (HBA) that the iSCSI initiator service uses to establish a discovery session and perform <b>SendTargets</b> requests. A value of <b>null</b> indicates that the iSCSI initiator service will use any HBA that is capable of accessing the target portal.

### -param InitiatorPortNumber [in, optional]

The port number on the HBA that the iSCSI initiator service use to perform <b>SendTargets</b> requests.

### -param Portal [in]

A pointer to a structure of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a> that specifies the target portal that the iSCSI initiator service removes from its list of portals.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RemoveIScsiSendTargetPortal as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
