---
UID: NF:msiquery.MsiSequenceW
title: MsiSequenceW function
author: windows-sdk-content
description: The MsiSequence function executes another action sequence, as described in the specified table.
old-location: setup\msisequence.htm
old-project: msi
ms.assetid: affb33ab-1b58-4d18-a908-8eaedb9ce1ca
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MsiSequence, MsiSequence function, MsiSequenceA, MsiSequenceW, _msi_msisequence, msiquery/MsiSequence, msiquery/MsiSequenceA, msiquery/MsiSequenceW, setup.msisequence
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
req.unicode-ansi: MsiSequenceW (Unicode) and MsiSequenceA (ANSI)
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
 - MsiSequence
 - MsiSequenceA
 - MsiSequenceW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSequenceW function


## -description


The 
<b>MsiSequence</b> function executes another action sequence, as described in the specified table.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szTable [in]

Specifies the name of the table containing the action sequence.


### -param iSequenceMode [in]

This parameter is currently unimplemented. It is reserved for future use and must be 0.


## -returns



This function returns UINT.




## -remarks



The 
<b>MsiSequence</b> function queries the specified table, ordering the actions by the numbers in the Sequence column. For each row retrieved, an action is executed, provided that any supplied condition expression does not evaluate to FALSE.

An action sequence containing any actions that update the system, such as the 
<a href="https://msdn.microsoft.com/187ad82f-13f5-4ea3-913c-2ae7561a6ee6">InstallFiles</a> and 
<a href="https://msdn.microsoft.com/ab121de3-f07d-401a-b52a-246a555c142c">WriteRegistryValues</a> actions, cannot be run by calling 
<b>MsiSequence</b>. The exception to this rule is if 
<b>MsiSequence</b> is called from a custom action that is scheduled in the 
<a href="https://msdn.microsoft.com/995d4159-bfc9-48b2-8328-3ae8251d785d">InstallExecuteSequence table</a> between the 
<a href="https://msdn.microsoft.com/c2637070-3fd9-422c-9252-cf15045c6485">InstallInitialize</a> and 
<a href="https://msdn.microsoft.com/ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6">InstallFinalize actions</a>. Actions that do not update the system, such as 
<a href="https://msdn.microsoft.com/56665876-2c74-476b-aa1a-158c6e86418d">AppSearch</a> or 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize</a>, can be called.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Installer Action Functions</a>
 

 

