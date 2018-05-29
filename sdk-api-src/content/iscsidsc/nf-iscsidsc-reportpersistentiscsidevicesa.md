---
UID: NF:iscsidsc.ReportPersistentIScsiDevicesA
title: ReportPersistentIScsiDevicesA function
author: windows-sdk-content
description: The ReportPersistentIscsiDevices function retrieves the list of persistently bound volumes and devices.
old-location: iscsidisc\reportpersistentiscsidevices.htm
old-project: iSCSIDisc
ms.assetid: 856e240d-8c4d-4e55-aef3-71f98193c221
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ReportPersistentIScsiDevicesA, ReportPersistentIscsiDevices, ReportPersistentIscsiDevices function [iSCSI Discovery Library API], ReportPersistentIscsiDevicesA, ReportPersistentIscsiDevicesW, iscsidisc.reportpersistentiscsidevices, iscsidsc/ReportPersistentIscsiDevices, iscsidsc/ReportPersistentIscsiDevicesA, iscsidsc/ReportPersistentIscsiDevicesW
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
req.unicode-ansi: ReportPersistentIscsiDevicesW (Unicode) and ReportPersistentIscsiDevicesA (ANSI)
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
-	ReportPersistentIscsiDevices
-	ReportPersistentIscsiDevicesA
-	ReportPersistentIscsiDevicesW
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# ReportPersistentIScsiDevicesA function


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




<a href="https://msdn.microsoft.com/184b256b-0cb0-45c1-8f73-5ff28fb388fb">AddPersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/9e21dde6-face-40ae-803b-2aa7861e6f4f">ClearPersistentIscsiDevices</a>



<a href="https://msdn.microsoft.com/2522f906-2a91-4d5b-8d6b-86e22c707046">RemoveIscsiPersistentTarget</a>



<a href="https://msdn.microsoft.com/4016d8e4-de67-4c49-b54f-31c1b7bd64a8">RemovePersistentIscsiDevice</a>



<a href="https://msdn.microsoft.com/0ab1a864-b44e-4307-9f7c-93cc0d40ff3a">ReportIscsiPersistentLogins</a>



<a href="https://msdn.microsoft.com/b21e5872-24b2-4a4c-86a7-528789c1b9aa">SetupPersistentIscsiDevices</a>
 

 

