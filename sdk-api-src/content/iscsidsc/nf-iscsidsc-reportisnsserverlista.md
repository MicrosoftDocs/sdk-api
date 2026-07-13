---
UID: NF:iscsidsc.ReportISNSServerListA
title: ReportISNSServerListA function (iscsidsc.h)
description: ReportIsnsServerList function retrieves the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service queries for discovered targets. (ANSI)
helpviewer_keywords: ["ReportISNSServerListA", "ReportIsnsServerListA", "iscsidsc/ReportIsnsServerListA"]
old-location: iscsidisc\reportisnsserverlist.htm
tech.root: iSCSIDisc
ms.assetid: 4fa773ac-0d3e-4860-8603-cb36e9278e93
ms.date: 12/05/2018
ms.keywords: ReportISNSServerListA, ReportIsnsServerList, ReportIsnsServerList function [iSCSI Discovery Library API], ReportIsnsServerListA, ReportIsnsServerListW, iscsidisc.reportisnsserverlist, iscsidsc/ReportIsnsServerList, iscsidsc/ReportIsnsServerListA, iscsidsc/ReportIsnsServerListW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportIsnsServerListW (Unicode) and ReportIsnsServerListA (ANSI)
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
 - ReportISNSServerListA
 - iscsidsc/ReportISNSServerListA
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
 - ReportIsnsServerList
 - ReportIsnsServerListA
 - ReportIsnsServerListW
---

# ReportISNSServerListA function


## -description

The <b>ReportIsnsServerList</b> function retrieves the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service queries for discovered targets.

## -parameters

### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 
If the operation succeeds, this location receives the size, represented by a number of  elements, that corresponds to the number of retrieved iSNS servers.

### -param Buffer [out]

The buffer that holds the list of iSNS servers on output. Each server name is <b>null</b> terminated, except for the last server name, which is double <b>null</b> terminated.

## -returns

Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is too small to hold the output data. 

Otherwise, <b>ReportIsnsServerList</b> returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addisnsservera">AddIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-refreshisnsservera">RefreshIsnsServer</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeisnsservera">RemoveIsnsServer</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportISNSServerList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
