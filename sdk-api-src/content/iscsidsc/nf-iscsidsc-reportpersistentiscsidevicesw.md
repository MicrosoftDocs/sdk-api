---
UID: NF:iscsidsc.ReportPersistentIScsiDevicesW
title: ReportPersistentIScsiDevicesW function (iscsidsc.h)
description: The ReportPersistentIscsiDevices function retrieves the list of persistently bound volumes and devices. (Unicode)
helpviewer_keywords: ["ReportPersistentIScsiDevicesW", "ReportPersistentIscsiDevices", "ReportPersistentIscsiDevices function [iSCSI Discovery Library API]", "ReportPersistentIscsiDevicesW", "iscsidisc.reportpersistentiscsidevices", "iscsidsc/ReportPersistentIscsiDevices", "iscsidsc/ReportPersistentIscsiDevicesW"]
old-location: iscsidisc\reportpersistentiscsidevices.htm
tech.root: iSCSIDisc
ms.assetid: 856e240d-8c4d-4e55-aef3-71f98193c221
ms.date: 12/05/2018
ms.keywords: ReportPersistentIScsiDevicesW, ReportPersistentIscsiDevices, ReportPersistentIscsiDevices function [iSCSI Discovery Library API], ReportPersistentIscsiDevicesA, ReportPersistentIscsiDevicesW, iscsidisc.reportpersistentiscsidevices, iscsidsc/ReportPersistentIscsiDevices, iscsidsc/ReportPersistentIscsiDevicesA, iscsidsc/ReportPersistentIscsiDevicesW
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportPersistentIscsiDevicesW (Unicode) and ReportPersistentIscsiDevicesA (ANSI)
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
 - ReportPersistentIScsiDevicesW
 - iscsidsc/ReportPersistentIScsiDevicesW
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
 - ReportPersistentIscsiDevices
 - ReportPersistentIscsiDevicesA
 - ReportPersistentIscsiDevicesW
---

# ReportPersistentIScsiDevicesW function


## -description

The <b>ReportPersistentIscsiDevices</b> function retrieves the list of persistently bound volumes and devices.

## -parameters

### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter.

### -param Buffer [out]

Pointer to a buffer that receives the list of volumes and devices that are persistently bound. The list consists of <b>null</b>-terminated strings. The last string, however, is double <b>null</b>-terminated.

## -returns

Returns ERROR_SUCCESS if the operation succeeds or ERROR_INSUFFICIENT_BUFFER if the buffer was insufficient to receive the output data. Otherwise, <b>ReportPersistentiScsiDevices</b> returns the appropriate Win32 or iSCSI error code on failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-addpersistentiscsidevicea">AddPersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-clearpersistentiscsidevices">ClearPersistentIscsiDevices</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removeiscsipersistenttargeta">RemoveIscsiPersistentTarget</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-removepersistentiscsidevicea">RemovePersistentIscsiDevice</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-reportiscsipersistentloginsa">ReportIscsiPersistentLogins</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-setuppersistentiscsidevices">SetupPersistentIscsiDevices</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ReportPersistentIScsiDevices as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
