---
UID: NF:taskschd.IPrincipal2.AddRequiredPrivilege
title: IPrincipal2::AddRequiredPrivilege (taskschd.h)
author: windows-sdk-content
description: Adds the required privilege to the task process token.
old-location: taskschd\iprincipal2_addrequiredprivilege.htm
tech.root: taskschd
ms.assetid: 74b7fffa-7e16-43e1-9176-677d9948f448
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRequiredPrivilege, AddRequiredPrivilege method [Task Scheduler], AddRequiredPrivilege method [Task Scheduler],IPrincipal2 interface, IPrincipal2 interface [Task Scheduler],AddRequiredPrivilege method, IPrincipal2.AddRequiredPrivilege, IPrincipal2::AddRequiredPrivilege, taskschd.iprincipal2_addrequiredprivilege, taskschd/IPrincipal2::AddRequiredPrivilege
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IPrincipal2.AddRequiredPrivilege
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrincipal2::AddRequiredPrivilege


## -description


Adds the  required privilege to the task process token.


## -parameters




### -param privilege [in]

Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/480f8038-0f67-4a69-b6f6-d7ba881d9d57">IPrincipal2</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

