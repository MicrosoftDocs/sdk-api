---
UID: NF:taskschd.IPrincipal2.AddRequiredPrivilege
title: IPrincipal2::AddRequiredPrivilege (taskschd.h)
description: Adds the required privilege to the task process token.
helpviewer_keywords: ["AddRequiredPrivilege","AddRequiredPrivilege method [Task Scheduler]","AddRequiredPrivilege method [Task Scheduler]","IPrincipal2 interface","IPrincipal2 interface [Task Scheduler]","AddRequiredPrivilege method","IPrincipal2.AddRequiredPrivilege","IPrincipal2::AddRequiredPrivilege","taskschd.iprincipal2_addrequiredprivilege","taskschd/IPrincipal2::AddRequiredPrivilege"]
old-location: taskschd\iprincipal2_addrequiredprivilege.htm
tech.root: taskschd
ms.assetid: 74b7fffa-7e16-43e1-9176-677d9948f448
ms.date: 12/05/2018
ms.keywords: AddRequiredPrivilege, AddRequiredPrivilege method [Task Scheduler], AddRequiredPrivilege method [Task Scheduler],IPrincipal2 interface, IPrincipal2 interface [Task Scheduler],AddRequiredPrivilege method, IPrincipal2.AddRequiredPrivilege, IPrincipal2::AddRequiredPrivilege, taskschd.iprincipal2_addrequiredprivilege, taskschd/IPrincipal2::AddRequiredPrivilege
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrincipal2::AddRequiredPrivilege
 - taskschd/IPrincipal2::AddRequiredPrivilege
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IPrincipal2.AddRequiredPrivilege
---

# IPrincipal2::AddRequiredPrivilege


## -description

Adds the  required privilege to the task process token.

## -parameters

### -param privilege [in]

Specifies the right of a task to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal2">IPrincipal2</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>