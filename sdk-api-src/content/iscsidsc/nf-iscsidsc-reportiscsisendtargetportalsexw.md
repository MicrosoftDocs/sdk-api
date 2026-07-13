---
UID: NF:iscsidsc.ReportIScsiSendTargetPortalsExW
title: ReportIScsiSendTargetPortalsExW function (iscsidsc.h)
description: ReportIscsiSendTargetPortalsEx function retrieves a list of static target portals that the iSCSI initiator service uses to perform automatic discovery with SendTarget requests. (Unicode)
helpviewer_keywords: ["ReportIScsiSendTargetPortalsExW", "ReportIscsiSendTargetPortalsEx", "ReportIscsiSendTargetPortalsEx function [iSCSI Discovery Library API]", "ReportIscsiSendTargetPortalsExW", "iscsidisc.reportiscsisendtargetportalsex", "iscsidsc/ReportIscsiSendTargetPortalsEx", "iscsidsc/ReportIscsiSendTargetPortalsExW"]
old-location: iscsidisc\reportiscsisendtargetportalsex.htm
tech.root: iSCSIDisc
ms.assetid: bf67ff5c-77b5-42ec-81b3-86b98e216d81
ms.date: 12/05/2018
ms.keywords: ReportIScsiSendTargetPortalsExW, ReportIscsiSendTargetPortalsEx, ReportIscsiSendTargetPortalsEx function [iSCSI Discovery Library API], ReportIscsiSendTargetPortalsExA, ReportIscsiSendTargetPortalsExW, iscsidisc.reportiscsisendtargetportalsex, iscsidsc/ReportIscsiSendTargetPortalsEx, iscsidsc/ReportIscsiSendTargetPortalsExA, iscsidsc/ReportIscsiSendTargetPortalsExW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiSendTargetPortalsExW (Unicode) and ReportIscsiSendTargetPortalsExA (ANSI)
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
 - ReportIScsiSendTargetPortalsExW
 - iscsidsc/ReportIScsiSendTargetPortalsExW
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
 - ReportIscsiSendTargetPortalsEx
 - ReportIscsiSendTargetPortalsExA
 - ReportIscsiSendTargetPortalsExW
---

# ReportIScsiSendTargetPortalsExW function


## -description

The <b>ReportIscsiSendTargetPortalsEx</b> function  retrieves a list of static target portals that the iSCSI initiator service uses to perform automatic discovery with <b>SendTarget</b> requests.

## -parameters

### -param PortalCount [out]

A pointer to a location that, on input, contains the number of entries in the <i>PortalInfo</i> array. On output, this parameter specifies the number of elements that contain return data.

### -param PortalInfoSize [in, out]

A pointer to a location that, on input, contains the byte-size of the buffer specified by <i>PortalInfo</i>. On output, this parameter specifies the number of bytes retrieved.

### -param PortalInfo [in, out]

Pointer to an array of elements contained in a <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_infoa">ISCSI_TARGET_PORTAL_INFO_EX</a> structure that describe the portals that the iSCSI initiator service utilizes to perform discovery with <b>SendTargets</b> requests.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the size of the buffer at <i>PortalInfo</i> is insufficient to contain the output data. Otherwise, <b>ReportIscsiSendTargetPortalsEx</b> returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portal_infoa">ISCSI_TARGET_PORTAL_INFO_EX</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportIScsiSendTargetPortalsEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
