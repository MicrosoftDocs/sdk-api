---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# MsiDoActionA function


## -description


The 
<b>MsiDoAction</b> function executes a built-in action, custom action, or user-interface wizard action.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szAction [in]

Specifies the action to execute.


## -returns



This function returns UINT.




## -remarks



The 
<b>MsiDoAction</b> function executes the action that corresponds to the name supplied. If the name is not recognized by the installer as a built-in action or as a custom action in the 
<a href="https://msdn.microsoft.com/0f47abc1-4e06-4ddc-9ea1-9afb9f27d499">CustomAction table</a>, the name is passed to the user-interface handler object, which can invoke a function or a dialog box. If a null action name is supplied, the installer uses the upper-case value of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">ACTION</a> property as the action to perform. If no property value is defined, the default action is performed, defined as "INSTALL".

Actions that update the system, such as the 
<a href="https://msdn.microsoft.com/187ad82f-13f5-4ea3-913c-2ae7561a6ee6">InstallFiles</a> and 
<a href="https://msdn.microsoft.com/ab121de3-f07d-401a-b52a-246a555c142c">WriteRegistryValues</a> actions, cannot be run by calling 
<b>MsiDoAction</b>. The exception to this rule is if 
<b>MsiDoAction</b> is called from a custom action that is scheduled in the 
<a href="https://msdn.microsoft.com/995d4159-bfc9-48b2-8328-3ae8251d785d">InstallExecuteSequence table</a> between the 
<a href="https://msdn.microsoft.com/c2637070-3fd9-422c-9252-cf15045c6485">InstallInitialize</a> and 
<a href="https://msdn.microsoft.com/ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6">InstallFinalize actions</a>. Actions that do not update the system, such as 
<a href="https://msdn.microsoft.com/56665876-2c74-476b-aa1a-158c6e86418d">AppSearch</a> or 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize</a>, can be called.




## -see-also




<a href="database_functions.htm">Installer Action Functions</a>
 

 

