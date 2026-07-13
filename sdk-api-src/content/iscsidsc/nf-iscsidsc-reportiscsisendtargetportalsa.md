---
UID: NF:iscsidsc.ReportIScsiSendTargetPortalsA
title: ReportIScsiSendTargetPortalsA function (iscsidsc.h)
description: ReportIscsiSendTargetPortals function retrieves a list of target portals that the iSCSI initiator service uses to perform automatic discovery with SendTarget requests. (ANSI)
helpviewer_keywords: ["ReportIScsiSendTargetPortalsA", "ReportIscsiSendTargetPortalsA", "iscsidsc/ReportIscsiSendTargetPortalsA"]
old-location: iscsidisc\reportiscsisendtargetportals.htm
tech.root: iSCSIDisc
ms.assetid: f082acc3-98d6-4758-aded-cb83e150e6d1
ms.date: 12/05/2018
ms.keywords: ReportIScsiSendTargetPortalsA, ReportIscsiSendTargetPortals, ReportIscsiSendTargetPortals function [iSCSI Discovery Library API], ReportIscsiSendTargetPortalsA, ReportIscsiSendTargetPortalsW, iscsidisc.reportiscsisendtargetportals, iscsidsc/ReportIscsiSendTargetPortals, iscsidsc/ReportIscsiSendTargetPortalsA, iscsidsc/ReportIscsiSendTargetPortalsW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiSendTargetPortalsW (Unicode) and ReportIscsiSendTargetPortalsA (ANSI)
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
 - ReportIScsiSendTargetPortalsA
 - iscsidsc/ReportIScsiSendTargetPortalsA
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
 - ReportIscsiSendTargetPortals
 - ReportIscsiSendTargetPortalsA
 - ReportIscsiSendTargetPortalsW
---

# ReportIScsiSendTargetPortalsA function


## -description

The <b>ReportIscsiSendTargetPortals</b> function retrieves a list of target portals that the iSCSI initiator service uses to perform automatic discovery with <b>SendTarget</b> requests.

## -parameters

### -param PortalCount [out]

A pointer to a location that, on input, contains the number of entries in the <i>PortalInfo</i> array. On output, this parameter specifies the number of elements that contain return data.

### -param PortalInfo [in, out]

Pointer to an array of elements contained in <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_infoa">ISCSI_TARGET_PORTAL_INFO</a> structures that describe the portals that the iSCSI initiator service utilizes to perform discovery with <b>SendTargets</b> requests.

## -returns

 Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size of Buffer is insufficient to contain the output data.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_infoa">ISCSI_TARGET_PORTAL_INFO</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportIScsiSendTargetPortals as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
