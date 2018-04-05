---
UID: NF:instance.CInstance.GetStatus
title: CInstance::GetStatus method
author: windows-driver-content
description: The GetStatus method determines whether a property exists and, if so, determines its type.
old-location: wmi\cinstance_getstatus.htm
old-project: WmiSdk
ms.assetid: 355386c5-7cd2-46de-8696-a83bd3f96cc5
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: CInstance, CInstance interface [Windows Management Instrumentation], GetStatus method, CInstance::GetStatus, GetStatus method [Windows Management Instrumentation], GetStatus method [Windows Management Instrumentation], CInstance interface, GetStatus,CInstance.GetStatus, _hmm_cinstance_getstatus, instance/CInstance::GetStatus, wmi.cinstance_getstatus
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
req.typenames: InputScope
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CInstance.GetStatus
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::GetStatus method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetStatus</b> method determines whether a property exists and, if so, determines its type.


## -parameters




### -param name

Name of the property to verify.


### -param a_Exists [ref]

<b>TRUE</b> if property exists and <b>FALSE</b> if the property does not exist.


### -param a_VarType

Type of property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> otherwise.



