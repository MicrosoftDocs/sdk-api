---
UID: NF:iscsidsc.ReportIScsiTargetsA
title: ReportIScsiTargetsA function (iscsidsc.h)
description: ReportIscsiTargets function retrieves the list of targets that the iSCSI initiator service has discovered, and can also instruct the iSCSI initiator service to refresh the list. (ANSI)
helpviewer_keywords: ["ReportIScsiTargetsA", "ReportIscsiTargetsA", "iscsidsc/ReportIscsiTargetsA"]
old-location: iscsidisc\reportiscsitargets.htm
tech.root: iSCSIDisc
ms.assetid: c4b2bcc4-d9d3-4fd3-bbca-03b13670054f
ms.date: 12/05/2018
ms.keywords: ReportIScsiTargetsA, ReportIscsiTargets, ReportIscsiTargets function [iSCSI Discovery Library API], ReportIscsiTargetsA, ReportIscsiTargetsW, iscsidisc.reportiscsitargets, iscsidsc/ReportIscsiTargets, iscsidsc/ReportIscsiTargetsA, iscsidsc/ReportIscsiTargetsW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiTargetsW (Unicode) and ReportIscsiTargetsA (ANSI)
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
 - ReportIScsiTargetsA
 - iscsidsc/ReportIScsiTargetsA
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
 - ReportIscsiTargets
 - ReportIscsiTargetsA
 - ReportIscsiTargetsW
---

# ReportIScsiTargetsA function


## -description

The <b>ReportIscsiTargets</b> function retrieves the list of targets that the iSCSI initiator service has discovered, and can also instruct the iSCSI initiator service to refresh the list.

## -parameters

### -param ForceUpdate [in]

If <b>true</b>, the iSCSI initiator service updates the list of discovered targets before returning the target list data to the caller.

### -param BufferSize [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter.

### -param Buffer [out]

Pointer to a buffer that receives and contains the list of targets. The list consists of <b>null</b>-terminated strings. The last string, however, is double <b>null</b>-terminated.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size is insufficient to contain  the output data. Otherwise, <b>ReportIscsiTargets</b> returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsisendtargetportalsa">ReportIscsiSendTargetPortals</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportIScsiTargets as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
