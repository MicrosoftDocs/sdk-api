---
UID: NS:winbase._UMS_SYSTEM_THREAD_INFORMATION
title: "_UMS_SYSTEM_THREAD_INFORMATION"
author: windows-sdk-content
description: Specifies a UMS scheduler thread, UMS worker thread, or non-UMS thread. The GetUmsSystemThreadInformation function uses this structure.
old-location: base\ums_system_thread_information.htm
tech.root: procthread
ms.assetid: eecdc592-5046-47c3-a4c6-ecb10899db3c
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PUMS_SYSTEM_THREAD_INFORMATION, PUMS_SYSTEM_THREAD_INFORMATION, PUMS_SYSTEM_THREAD_INFORMATION structure pointer, UMS_SYSTEM_THREAD_INFORMATION, UMS_SYSTEM_THREAD_INFORMATION structure, _UMS_SYSTEM_THREAD_INFORMATION, base.ums_system_thread_information, winbase/PUMS_SYSTEM_THREAD_INFORMATION, winbase/UMS_SYSTEM_THREAD_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps only],Windows 7 (64-bit only) and Windows Server 2008 R2 (64-bit only) with KB977165  installed
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - UMS_SYSTEM_THREAD_INFORMATION
product: Windows
targetos: Windows
req.typenames: UMS_SYSTEM_THREAD_INFORMATION, *PUMS_SYSTEM_THREAD_INFORMATION
req.redist: 
---

# _UMS_SYSTEM_THREAD_INFORMATION structure


## -description


Specifies a UMS scheduler thread, UMS worker thread, or non-UMS thread. The <a href="https://msdn.microsoft.com/7c8347b6-6546-4ea9-9b2a-11794782f482">GetUmsSystemThreadInformation</a> function uses this structure. 


## -struct-fields




### -field UmsVersion

The UMS version. This member must be UMS_VERSION.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsSchedulerThread

A bitfield that specifies a UMS scheduler thread. If <b>IsUmsSchedulerThread</b> is set, <b>IsUmsWorkerThread</b> must be clear. 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsWorkerThread

A bitfield that specifies a UMS worker thread. If <b>IsUmsWorkerThread</b>  is set, <b>IsUmsSchedulerThread</b> must be clear. 


### -field DUMMYUNIONNAME.ThreadUmsFlags

 




## -remarks



If both <b>IsUmsSchedulerThread</b>  and <b>IsUmsWorkerThread</b> are clear, the structure specifies a non-UMS thread. 



