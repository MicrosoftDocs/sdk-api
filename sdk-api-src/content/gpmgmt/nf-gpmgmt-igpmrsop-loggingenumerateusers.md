---
UID: NF:gpmgmt.IGPMRSOP.LoggingEnumerateUsers
title: IGPMRSOP::LoggingEnumerateUsers
author: windows-sdk-content
description: Enumerates all users who have logging mode data on a specific computer.
old-location: gpmc\igpmrsop_loggingenumerateusers.htm
tech.root: GPMC
ms.assetid: 7cc794e6-1a8d-4e31-9bea-4ebc4cf51602
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GPMRSOP class [GPMC],LoggingEnumerateUsers method, IGPMRSOP interface [GPMC],LoggingEnumerateUsers method, IGPMRSOP.LoggingEnumerateUsers, IGPMRSOP::LoggingEnumerateUsers, LoggingEnumerateUsers, LoggingEnumerateUsers method [GPMC], LoggingEnumerateUsers method [GPMC],GPMRSOP class, LoggingEnumerateUsers method [GPMC],IGPMRSOP interface, _win32_igpmrsop_loggingenumerateusers, gpmc.igpmrsop_loggingenumerateusers, gpmgmt/IGPMRSOP::LoggingEnumerateUsers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMRSOP.LoggingEnumerateUsers
 - GPMRSOP.LoggingEnumerateUsers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpmgmt.h
: 
- IGPMRSOP.LoggingEnumerateUsers
: 
---

# IGPMRSOP::LoggingEnumerateUsers


## -description


Enumerates all users who have logging mode data on a specific computer.


## -parameters




### -param varVal [out]

Pointer to a SAFEARRAY containing VARIANT members. Each VARIANT contains a Dispatch pointer to  the 
<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns an array of <b>GPMTrustee</b> object references. Note that the array is a normal array, not a GPMC collection.

<h3>VB</h3>
Returns an array of <b>GPMTrustee</b> object references. Note that the array is a normal array, not a GPMC collection.




## -see-also




<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>
 

 

