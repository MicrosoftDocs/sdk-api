---
UID: NF:gpmgmt.IGPMRSOP.LoggingEnumerateUsers
title: IGPMRSOP::LoggingEnumerateUsers (gpmgmt.h)
author: windows-sdk-content
description: Enumerates all users who have logging mode data on a specific computer.
old-location: gpmc\igpmrsop_loggingenumerateusers.htm
tech.root: gpmc
ms.assetid: 7cc794e6-1a8d-4e31-9bea-4ebc4cf51602
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMRSOP class [GPMC],LoggingEnumerateUsers method, IGPMRSOP interface [GPMC],LoggingEnumerateUsers method, IGPMRSOP.LoggingEnumerateUsers, IGPMRSOP::LoggingEnumerateUsers, LoggingEnumerateUsers, LoggingEnumerateUsers method [GPMC], LoggingEnumerateUsers method [GPMC],GPMRSOP class, LoggingEnumerateUsers method [GPMC],IGPMRSOP interface, _win32_igpmrsop_loggingenumerateusers, gpmc.igpmrsop_loggingenumerateusers, gpmgmt/IGPMRSOP::LoggingEnumerateUsers
ms.topic: method
f1_keywords: 
 - "gpmgmt/IGPMRSOP.LoggingEnumerateUsers"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMRSOP::LoggingEnumerateUsers


## -description


Enumerates all users who have logging mode data on a specific computer.


## -parameters




### -param varVal [out]

Pointer to a SAFEARRAY containing VARIANT members. Each VARIANT contains a Dispatch pointer to  the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns an array of <b>GPMTrustee</b> object references. Note that the array is a normal array, not a GPMC collection.

<h3>VB</h3>
Returns an array of <b>GPMTrustee</b> object references. Note that the array is a normal array, not a GPMC collection.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmrsop">IGPMRSOP</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
 

 

