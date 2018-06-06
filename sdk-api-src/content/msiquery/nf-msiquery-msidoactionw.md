---
UID: NF:msiquery.MsiDoActionW
title: MsiDoActionW function
author: windows-sdk-content
description: The MsiDoAction function executes a built-in action, custom action, or user-interface wizard action.
old-location: setup\msidoaction.htm
old-project: Msi
ms.assetid: 33f2de47-71ab-4da8-bd56-ee58cde86e2b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiDoAction, MsiDoAction function, MsiDoActionA, MsiDoActionW, _msi_msidoaction, msiquery/MsiDoAction, msiquery/MsiDoActionA, msiquery/MsiDoActionW, setup.msidoaction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDoActionW (Unicode) and MsiDoActionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiDoAction
 - MsiDoActionA
 - MsiDoActionW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiDoActionW function


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
 

 

