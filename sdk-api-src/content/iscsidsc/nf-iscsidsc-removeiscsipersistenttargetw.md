---
UID: NF:iscsidsc.RemoveIScsiPersistentTargetW
title: RemoveIScsiPersistentTargetW function (iscsidsc.h)
description: RemoveIscsiPersistentTarget function removes a persistent login for the specified hardware initiator Host Bus Adapter (HBA), initiator port, and target portal. (Unicode)
helpviewer_keywords: ["RemoveIScsiPersistentTargetW", "RemoveIscsiPersistentTarget", "RemoveIscsiPersistentTarget function [iSCSI Discovery Library API]", "RemoveIscsiPersistentTargetW", "iscsidisc.removeiscsipersistenttarget", "iscsidsc/RemoveIscsiPersistentTarget", "iscsidsc/RemoveIscsiPersistentTargetW"]
old-location: iscsidisc\removeiscsipersistenttarget.htm
tech.root: iSCSIDisc
ms.assetid: 2522f906-2a91-4d5b-8d6b-86e22c707046
ms.date: 12/05/2018
ms.keywords: RemoveIScsiPersistentTargetW, RemoveIscsiPersistentTarget, RemoveIscsiPersistentTarget function [iSCSI Discovery Library API], RemoveIscsiPersistentTargetA, RemoveIscsiPersistentTargetW, iscsidisc.removeiscsipersistenttarget, iscsidsc/RemoveIscsiPersistentTarget, iscsidsc/RemoveIscsiPersistentTargetA, iscsidsc/RemoveIscsiPersistentTargetW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveIscsiPersistentTargetW (Unicode) and RemoveIscsiPersistentTargetA (ANSI)
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
 - RemoveIScsiPersistentTargetW
 - iscsidsc/RemoveIScsiPersistentTargetW
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
 - RemoveIscsiPersistentTarget
 - RemoveIscsiPersistentTargetA
 - RemoveIscsiPersistentTargetW
---

# RemoveIScsiPersistentTargetW function


## -description

The <b>RemoveIscsiPersistentTarget</b> function removes a persistent login for the specified hardware initiator Host Bus Adapter (HBA), initiator port, and target portal.

## -parameters

### -param InitiatorInstance [in]

The name of the initiator that maintains the persistent login to remove.

### -param InitiatorPortNumber [in, optional]

The port number on which the initiator connects to <i>TargetName</i>. If <i>InitiatorPortNumber</i> is <b>ISCSI_ALL_INITIATOR_PORTS</b> the miniport driver for the initiator HBA removes the <i>TargetName</i> from the persistent login lists for all initiator ports.

### -param TargetName [in]

The name of the target.

### -param Portal [in]

The portal through which the initiator connects to the target. If <i>Portal</i> is <b>null</b> or contains no information, the miniport driver for the initiator HBA removes persistent logins for the target on all portals.

## -returns

Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removepersistentiscsidevicea">RemovePersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportpersistentiscsidevicesa">ReportPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines RemoveIScsiPersistentTarget as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
