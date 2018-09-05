---
UID: NF:photoacquire.IPhotoProgressActionCB.DoAction
title: DoAction function
author: windows-sdk-content
description: The DoAction method of the Session object executes the action function corresponding to the name supplied.
old-location: setup\session_doaction.htm
old-project: msi
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DoAction, DoAction method, DoAction method,Session object, Session object,DoAction method, Session.DoAction, _msi_doaction_method, setup.session_doaction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: photoacquire.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msi.dll
api_name:
 - Session.DoAction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msi.dll
req.irql: 
req.product: ADAM
---

# DoAction function


## -description


The 
<b>DoAction</b> method of the 
<a href="https://msdn.microsoft.com/013959d9-900c-45f7-b742-17b0365d6107">Session</a> object executes the action function corresponding to the name supplied. If a Null action name is supplied, the engine uses the uppercase value of the 
<a href="https://msdn.microsoft.com/f2c436b6-ebd9-4ac4-8609-f54129023ca7">ACTION property</a> as the action to perform. If no property value is defined, the default action is performed, currently defined as INSTALL. This method returns an integer enumeration.


## -parameters




### -param hWndParent

TBD




#### - action

Required string name of the action to execute. Case-sensitive.


## -returns



This method does not return a value.




## -remarks



Actions that update the system, such as the 
<a href="https://msdn.microsoft.com/187ad82f-13f5-4ea3-913c-2ae7561a6ee6">InstallFiles</a> and 
<a href="https://msdn.microsoft.com/ab121de3-f07d-401a-b52a-246a555c142c">WriteRegistryValues</a> actions, cannot be run by calling the 
<b>DoAction</b> method. The exception to this rule is if the 
<b>DoAction</b> method is called from a custom action that is scheduled in the 
<a href="https://msdn.microsoft.com/995d4159-bfc9-48b2-8328-3ae8251d785d">InstallExecuteSequence table</a> between the 
<a href="https://msdn.microsoft.com/c2637070-3fd9-422c-9252-cf15045c6485">InstallInitialize</a> and 
<a href="https://msdn.microsoft.com/ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6">InstallFinalize actions</a>. Actions that do not update the system, such as 
<a href="https://msdn.microsoft.com/56665876-2c74-476b-aa1a-158c6e86418d">AppSearch</a> or 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize</a>, can be called.



