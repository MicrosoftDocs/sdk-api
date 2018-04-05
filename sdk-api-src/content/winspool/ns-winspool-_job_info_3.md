---
UID: NS:winspool._JOB_INFO_3
title: "_JOB_INFO_3"
author: windows-driver-content
description: The JOB_INFO_3 structure is used to link together a set of print jobs.
old-location: gdi\job_info_3.htm
old-project: printdocs
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPJOB_INFO_3, *PJOB_INFO_3, JOB_INFO_3, JOB_INFO_3 structure [Windows GDI], PJOB_INFO_3, PJOB_INFO_3 structure pointer [Windows GDI], _JOB_INFO_3, _win32_JOB_INFO_3_str, gdi.job_info_3, winspool/JOB_INFO_3, winspool/PJOB_INFO_3"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: JOB_INFO_3, *PJOB_INFO_3, *LPJOB_INFO_3
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	JOB_INFO_3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _JOB_INFO_3 structure


## -description



The <b>JOB_INFO_3</b> structure is used to link together a set of print jobs.




## -struct-fields




### -field JobId

The print job identifier.


### -field NextJobId

The print job identifier for the next print job in the linked set of print jobs.


### -field Reserved

This value is reserved for future use. You must set it to zero.


## -see-also




<a href="https://msdn.microsoft.com/1cf429ea-b40e-4063-b6de-c43b7b87f3d3">EnumJobs</a>



<a href="https://msdn.microsoft.com/57e59f84-d2a0-4722-b0fc-6673f7bb5c57">GetJob</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/21947c69-c517-4962-8eb7-b45ed4211d9a">SetJob</a>
 

 

