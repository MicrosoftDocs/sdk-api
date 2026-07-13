---
UID: NF:iscsidsc.ReportIScsiInitiatorListW
title: ReportIScsiInitiatorListW function (iscsidsc.h)
description: ReportIscsiInitiatorList function retrieves the list of initiator Host Bus Adapters that are running on the machine. (Unicode)
helpviewer_keywords: ["ReportIScsiInitiatorListW", "ReportIscsiInitiatorList", "ReportIscsiInitiatorList function [iSCSI Discovery Library API]", "ReportIscsiInitiatorListW", "iscsidisc.reportiscsiinitiatorlist", "iscsidsc/ReportIscsiInitiatorList", "iscsidsc/ReportIscsiInitiatorListW"]
old-location: iscsidisc\reportiscsiinitiatorlist.htm
tech.root: iSCSIDisc
ms.assetid: 7039fab5-ac76-4420-994b-b8c18196b022
ms.date: 12/05/2018
ms.keywords: ReportIScsiInitiatorListW, ReportIscsiInitiatorList, ReportIscsiInitiatorList function [iSCSI Discovery Library API], ReportIscsiInitiatorListA, ReportIscsiInitiatorListW, iscsidisc.reportiscsiinitiatorlist, iscsidsc/ReportIscsiInitiatorList, iscsidsc/ReportIscsiInitiatorListA, iscsidsc/ReportIscsiInitiatorListW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIscsiInitiatorListW (Unicode) and ReportIscsiInitiatorListA (ANSI)
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
 - ReportIScsiInitiatorListW
 - iscsidsc/ReportIScsiInitiatorListW
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
 - ReportIscsiInitiatorList
 - ReportIscsiInitiatorListA
 - ReportIscsiInitiatorListW
---

# ReportIScsiInitiatorListW function


## -description

The <b>ReportIscsiInitiatorList</b> function retrieves the list of initiator Host Bus Adapters that are running on the machine.

## -parameters

### -param BufferSize [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 
If the operation succeeds, this location receives the size, represented by a number of elements, that corresponds to the retreived data.

### -param Buffer [out]

A buffer that, on output, is filled with the list of initiator names. Each initiator name is a <b>null</b>-terminated string, except for the last initiator name, which is double-<b>null</b> terminated.

## -returns

 Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer size of Buffer is insufficient to contain the output data.

 Otherwise, <b>ReportIscsiInitiatorList</b> returns the appropriate Win32 or iSCSI error code on failure.

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportIScsiInitiatorList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

