---
UID: NF:wbemdisp.ISWbemPrivilegeSet.Remove
title: ISWbemPrivilegeSet::Remove
author: windows-sdk-content
description: The Remove method of the SWbemPrivilegeSet object deletes a privilege from the collection.
old-location: wmi\swbemprivilegeset_remove.htm
old-project: WmiSdk
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemPrivilegeSet interface [Windows Management Instrumentation],Remove method, ISWbemPrivilegeSet.Remove, ISWbemPrivilegeSet::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],ISWbemPrivilegeSet interface, Remove method [Windows Management Instrumentation],SWbemPrivilegeSet object, SWbemPrivilegeSet object [Windows Management Instrumentation],Remove method, SWbemPrivilegeSet.Remove, _hmm_swbemprivilegeset.remove, wmi.swbemprivilegeset_remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemPrivilegeSet.Remove
 - ISWbemPrivilegeSet.Remove
 - ISWbemPrivilegeSet.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPrivilegeSet::Remove


## -description


The 
<b>Remove</b> method of the 
<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a> object deletes a privilege from the collection.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iPrivilege

Required. This is one of the WMI constants from the 
<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a> group. These constants are essentially integers that represent specific privileges. For example, to remove the privilege that allows you to shut down a Windows system, use the <b>wbemPrivilegeShutdown</b> constant or the numeric equivalent of 0x17.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a>



<a href="https://msdn.microsoft.com/7d44193f-60e1-4e83-8640-31d8df509d98">SWbemPrivilegeSet.Add</a>
 

 

