---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _QUOTA_LIMITS structure


## -description


The <b>QUOTA_LIMITS</b> structure describes the amount of system resources available to a user.


## -struct-fields




### -field PagedPoolLimit

Specifies the amount of paged pool memory assigned to the user. The paged pool is an area of system memory (physical memory used by the operating system) for objects that can be written to disk when they are not being used.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.


### -field NonPagedPoolLimit

Specifies the amount of nonpaged pool memory assigned to the user. The nonpaged pool is an area of system memory  for objects that cannot be written to disk but must remain in physical memory as long as they are allocated.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.


### -field MinimumWorkingSetSize

Specifies the minimum set size assigned to the user. The "working set" of a process is the set of memory pages currently visible to the process in physical RAM memory. These pages are present in memory when the application is running and available for an application to use without triggering a page fault.

The value set in this member is not enforced by the LSA. You should set this member to <b>NULL</b>, which causes the default value to be used.


### -field MaximumWorkingSetSize

Specifies the maximum set size assigned to the user.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.


### -field PagefileLimit

Specifies the maximum size, in bytes, of the paging file, which is a reserved space on disk that backs up committed physical memory on the computer.

The value set in this member is not enforced by the LSA. You should set this member to 0, which causes the default value to be used.


### -field TimeLimit

Indicates the maximum amount of time the process can run.

The value set in this member is not enforced by the LSA. You should set this member to <b>NULL</b>, which causes the default value to be used.

