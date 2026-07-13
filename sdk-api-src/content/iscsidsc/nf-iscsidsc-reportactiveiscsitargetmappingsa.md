---
UID: NF:iscsidsc.ReportActiveIScsiTargetMappingsA
title: ReportActiveIScsiTargetMappingsA function (iscsidsc.h)
description: ReportActiveIscsiTargetMappings function retrieves the target mappings that are currently active for all initiators on the computer. (ANSI)
helpviewer_keywords: ["ReportActiveIScsiTargetMappingsA", "ReportActiveIscsiTargetMappingsA", "iscsidsc/ReportActiveIscsiTargetMappingsA"]
old-location: iscsidisc\reportactiveiscsitargetmappings.htm
tech.root: iSCSIDisc
ms.assetid: 24de0e43-ba16-4598-92c5-ea17da17e030
ms.date: 12/05/2018
ms.keywords: ReportActiveIScsiTargetMappingsA, ReportActiveIscsiTargetMappings, ReportActiveIscsiTargetMappings function [iSCSI Discovery Library API], ReportActiveIscsiTargetMappingsA, ReportActiveIscsiTargetMappingsW, iscsidisc.reportactiveiscsitargetmappings, iscsidsc/ReportActiveIscsiTargetMappings, iscsidsc/ReportActiveIscsiTargetMappingsA, iscsidsc/ReportActiveIscsiTargetMappingsW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportActiveIscsiTargetMappingsW (Unicode) and ReportActiveIscsiTargetMappingsA (ANSI)
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
 - ReportActiveIScsiTargetMappingsA
 - iscsidsc/ReportActiveIScsiTargetMappingsA
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
 - ReportActiveIscsiTargetMappings
 - ReportActiveIscsiTargetMappingsA
 - ReportActiveIscsiTargetMappingsW
---

# ReportActiveIScsiTargetMappingsA function


## -description

<b>ReportActiveIscsiTargetMappings</b> function retrieves the target mappings that are currently active for all initiators on the computer.

## -parameters

### -param BufferSize [in, out]

A pointer to a location that, on input, contains the size, in bytes, of the buffer that <i>Mappings</i> points to. If the operation succeeds, the location receives the size, in bytes, of the mapping data that was retrieved. If the buffer  that <i>Mappings</i> points to is not sufficient to contain the output data, the location receives the buffer size, in bytes, that is required.

### -param MappingCount [out]

If the operation succeeds, the location pointed to by <i>MappingCount</i> receives the number of mappings that were retrieved.

### -param Mappings [out]

A pointer to an array of type <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a> that, on output, is filled with the active target mappings for all initiators.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is not large enough.

Otherwise, <b>ReportActiveIscsiTargetMappings</b> returns the appropriate Win32 or iSCSI error code on failure.

## -remarks

Target mappings associate bus, target and LUN numbers with the LUNs on a target device.







> [!NOTE]
> The iscsidsc.h header defines ReportActiveIScsiTargetMappings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_mappinga">ISCSI_TARGET_MAPPING</a>
