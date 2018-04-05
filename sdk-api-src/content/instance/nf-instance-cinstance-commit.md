---
UID: NF:instance.CInstance.Commit
title: CInstance::Commit method
author: windows-driver-content
description: The Commit method returns the current instance to WMI.
old-location: wmi\cinstance_commit.htm
old-project: WmiSdk
ms.assetid: 699dadf9-18b5-4c6d-a5c4-59ea8a85f089
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: "?Commit@CInstance@@QAEJXZ, ?Commit@CInstance@@QEAAJXZ, CInstance, CInstance interface [Windows Management Instrumentation], Commit method, CInstance::Commit, Commit method [Windows Management Instrumentation], Commit method [Windows Management Instrumentation], CInstance interface, Commit,CInstance.Commit, _hmm_cinstance_commit, instance/CInstance::Commit, wmi.cinstance_commit"
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
-	CInstance.Commit
-	?Commit@CInstance@@QAEJXZ
-	?Commit@CInstance@@QEAAJXZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::Commit method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Commit</b> method returns the current instance to WMI.


## -parameters






## -returns



Use the <b>SUCCEEDED</b> or <b>FAILED</b> macro on the returned <b>HRESULT</b> to determine success or failure of the method.




## -remarks



If the client cancels the query, the <b>Commit</b> method returns an error. A provider writer can use this fact to terminate an enumeration.

Also, framework providers should call this method to commit rather than <a href="https://msdn.microsoft.com/619adf78-26db-4a90-90ba-bdacb3e55975">Provider::Commit</a>.  <b>Provider::Commit</b> calls <b>CInstance::Release</b> automatically. Smart <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> pointers cannot be used in this case because the smart <b>CInstance</b> pointer would call <b>CInstance::Release</b> in its destructor. If the release has already occurred, an exception will result. Issues of this type are best resolved by allowing the <b>CInstance</b> instance, or a smart pointer to it, to call <b>CInstance::Release</b> when it is appropriate.



