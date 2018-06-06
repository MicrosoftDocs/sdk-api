---
UID: NF:iscsidsc.ReportIScsiInitiatorListA
title: ReportIScsiInitiatorListA function
author: windows-sdk-content
description: ReportIscsiInitiatorList function retrieves the list of initiator Host Bus Adapters that are running on the machine.
old-location: iscsidisc\reportiscsiinitiatorlist.htm
old-project: iSCSIDisc
ms.assetid: 7039fab5-ac76-4420-994b-b8c18196b022
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ReportIScsiInitiatorListA, ReportIscsiInitiatorList, ReportIscsiInitiatorList function [iSCSI Discovery Library API], ReportIscsiInitiatorListA, ReportIscsiInitiatorListW, iscsidisc.reportiscsiinitiatorlist, iscsidsc/ReportIscsiInitiatorList, iscsidsc/ReportIscsiInitiatorListA, iscsidsc/ReportIscsiInitiatorListW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
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
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# ReportIScsiInitiatorListA function


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



