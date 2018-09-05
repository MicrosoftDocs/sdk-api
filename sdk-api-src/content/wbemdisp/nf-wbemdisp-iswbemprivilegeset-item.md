---
UID: NF:wbemdisp.ISWbemPrivilegeSet.Item
title: ISWbemPrivilegeSet::Item
author: windows-sdk-content
description: The Item method of the SWbemPrivilegeSet object returns an SWbemPrivilege object from the collection. The Item method is the default method of an SWbemPrivilegeSet object.
old-location: wmi\swbemprivilegeset_item.htm
old-project: WmiSdk
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemPrivilegeSet interface [Windows Management Instrumentation],Item method, ISWbemPrivilegeSet.Item, ISWbemPrivilegeSet::Item, Item, Item method [Windows Management Instrumentation], Item method [Windows Management Instrumentation],ISWbemPrivilegeSet interface, Item method [Windows Management Instrumentation],SWbemPrivilegeSet object, SWbemPrivilegeSet object [Windows Management Instrumentation],Item method, SWbemPrivilegeSet.Item, _hmm_swbemprivilegeset.item, wmi.swbemprivilegeset_item
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
 - SWbemPrivilegeSet.Item
 - ISWbemPrivilegeSet.Item
 - ISWbemPrivilegeSet.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPrivilegeSet::Item


## -description


The 
<b>Item</b> method of the 
<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a> object returns an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object from the collection. The 
<b>Item</b> method is the default method of an <b>SWbemPrivilegeSet</b> object.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iPrivilege

Required. One of the WMI constants from the 
<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a> group. These constants are essentially integers that represent specific privileges. For example, to get the privilege that allows you to shut down a Windows system, use the <b>wbemPrivilegeShutdown</b> constant or the numeric equivalent of 23 (0x17).


### -param objWbemPrivilege






## -returns



If successful, the requested 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object is returned.




## -see-also




<a href="https://msdn.microsoft.com/11bb8723-f329-4083-8219-2256ce44a5e3">Executing Privileged Operations</a>



<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a>



<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a>
 

 

