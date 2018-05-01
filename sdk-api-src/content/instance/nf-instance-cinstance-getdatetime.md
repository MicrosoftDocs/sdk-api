---
UID: NF:instance.CInstance.GetDateTime
title: CInstance::GetDateTime method
author: windows-driver-content
description: The GetDateTime method returns a datetime property.
old-location: wmi\cinstance_getdatetime.htm
old-project: WmiSdk
ms.assetid: b7474d1c-4ed9-4669-a0e6-01230a3bf8fa
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: CInstance, CInstance interface [Windows Management Instrumentation], GetDateTime method, CInstance::GetDateTime, GetDateTime method [Windows Management Instrumentation], GetDateTime method [Windows Management Instrumentation], CInstance interface, GetDateTime,CInstance.GetDateTime, _hmm_cinstance_getdatetime, instance/CInstance::GetDateTime, wmi.cinstance_getdatetime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: instance.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TrustLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CInstance.GetDateTime
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::GetDateTime method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetDateTime</b> method returns a datetime property.


## -parameters




### -param name

Name of the datetime property retrieved.


### -param wbemtime [ref]

Buffer to receive the datetime property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a datetime value or a property that does not exist. More information is available in the log file, Framework.log.



