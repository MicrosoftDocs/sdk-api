---
UID: NF:iscsidsc.ReportIScsiTargetPortalsA
title: ReportIScsiTargetPortalsA function (iscsidsc.h)
description: ReportIscsiTargetPortals function retrieves target portal information discovered by the iSCSI initiator service. (ANSI)
helpviewer_keywords: ["ReportIScsiTargetPortalsA", "ReportIscsiTargetPortalsA", "iscsidsc/ReportIscsiTargetPortalsA"]
old-location: iscsidisc\reportiscsitargetportals.htm
tech.root: iSCSIDisc
ms.assetid: e52d095d-4c05-490e-bdc3-639198a93335
ms.date: 12/05/2018
ms.keywords: ReportIScsiTargetPortalsA, ReportIscsiTargetPortals, ReportIscsiTargetPortals function [iSCSI Discovery Library API], ReportIscsiTargetPortalsA, ReportIscsiTargetPortalsW, iscsidisc.reportiscsitargetportals, iscsidsc/ReportIscsiTargetPortals, iscsidsc/ReportIscsiTargetPortalsA, iscsidsc/ReportIscsiTargetPortalsW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiTargetPortalsW (Unicode) and ReportIscsiTargetPortalsA (ANSI)
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
 - ReportIScsiTargetPortalsA
 - iscsidsc/ReportIScsiTargetPortalsA
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
 - ReportIscsiTargetPortals
 - ReportIscsiTargetPortalsA
 - ReportIscsiTargetPortalsW
---

# ReportIScsiTargetPortalsA function


## -description

The <b>ReportIscsiTargetPortals</b> function retrieves target portal information discovered by the iSCSI initiator service.

## -parameters

### -param InitiatorName [in, optional]

A string that represents the name of the initiator node.

### -param TargetName [in]

A string that represents the name of the target for which the portal information is retrieved.

### -param TargetPortalTag [in, optional]

A <b>USHORT</b> value that represents a tag associated with the portal.

### -param ElementCount [in, out]

A <b>ULONG</b> value that specifies the number of portals currently reported for the specified target.

### -param Portals [out]

A variable-length array of an <b>ISCSI_TARGET_PORTALW</b> structure. The number of elements contained in this array is specified by the value of <i>ElementCount</i>.

## -returns

Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.

## -see-also

<b>ISCSI_TARGET_PORTALW</b>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportIScsiTargetPortals as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

