---
UID: NF:wbemdisp.ISWbemPrivilege.get_Name
title: ISWbemPrivilege::get_Name
author: windows-sdk-content
description: The Name property of an SWbemPrivilege object is a string that uniquely describes a privilege.
old-location: wmi\swbemprivilege_name.htm
old-project: WmiSdk
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemPrivilege interface [Windows Management Instrumentation],Name property, ISWbemPrivilege.get_Name, ISWbemPrivilege::get_Name, Name property [Windows Management Instrumentation], Name property [Windows Management Instrumentation],ISWbemPrivilege interface, Name property [Windows Management Instrumentation],SWbemPrivilege object, SWbemPrivilege object [Windows Management Instrumentation],Name property, SWbemPrivilege.Name, _hmm_swbemprivilege.name, get_Name, wmi.swbemprivilege_name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
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
 - SWbemPrivilege.Name
 - ISWbemPrivilege.Name
 - ISWbemPrivilege.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPrivilege::get_Name


## -description


The 
<b>Name</b> property of an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object is a string that uniquely describes a privilege. For example, the privilege that controls whether a user can execute the shutdown method of an object has the "SeShutdownPrivilege" string in the <b>SWbemPrivilege.Name</b> property. This property is read-only.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters

