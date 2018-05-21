---
UID: NF:iscsidsc.ReportActiveIScsiTargetMappingsA
title: ReportActiveIScsiTargetMappingsA function
author: windows-driver-content
description: ReportActiveIscsiTargetMappings function retrieves the target mappings that are currently active for all initiators on the computer.
old-location: iscsidisc\reportactiveiscsitargetmappings.htm
old-project: iSCSIDisc
ms.assetid: 24de0e43-ba16-4598-92c5-ea17da17e030
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: ReportActiveIScsiTargetMappingsA, ReportActiveIscsiTargetMappings, ReportActiveIscsiTargetMappings function [iSCSI Discovery Library API], ReportActiveIscsiTargetMappingsA, ReportActiveIscsiTargetMappingsW, iscsidisc.reportactiveiscsitargetmappings, iscsidsc/ReportActiveIscsiTargetMappings, iscsidsc/ReportActiveIscsiTargetMappingsA, iscsidsc/ReportActiveIscsiTargetMappingsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	ReportActiveIscsiTargetMappings
-	ReportActiveIscsiTargetMappingsA
-	ReportActiveIscsiTargetMappingsW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
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

A pointer to an array of type <a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a> that, on output, is filled with the active target mappings for all initiators.


## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is not large enough.

Otherwise, <b>ReportActiveIscsiTargetMappings</b> returns the appropriate Win32 or iSCSI error code on failure.




## -remarks



Target mappings associate bus, target and LUN numbers with the LUNs on a target device.






## -see-also




<a href="https://msdn.microsoft.com/bdc27e67-1d64-42cd-adfa-a792012b7142">ISCSI_TARGET_MAPPING</a>
 

 

