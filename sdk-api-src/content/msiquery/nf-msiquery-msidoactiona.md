---
UID: NF:msiquery.MsiDoActionA
title: MsiDoActionA function (msiquery.h)
description: The MsiDoAction function executes a built-in action, custom action, or user-interface wizard action.
old-location: setup\msidoaction.htm
tech.root: Msi
ms.assetid: 33f2de47-71ab-4da8-bd56-ee58cde86e2b
ms.date: 12/05/2018
ms.keywords: MsiDoAction, MsiDoAction function, MsiDoActionA, MsiDoActionW, _msi_msidoaction, msiquery/MsiDoAction, msiquery/MsiDoActionA, msiquery/MsiDoActionW, setup.msidoaction
f1_keywords:
- msiquery/MsiDoAction
dev_langs:
- c++
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiDoActionA function


## -description


The 
<b>MsiDoAction</b> function executes a built-in action, custom action, or user-interface wizard action.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.


### -param szAction [in]

Specifies the action to execute.


## -returns



This function returns UINT.




## -remarks



The 
<b>MsiDoAction</b> function executes the action that corresponds to the name supplied. If the name is not recognized by the installer as a built-in action or as a custom action in the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/customaction-table">CustomAction table</a>, the name is passed to the user-interface handler object, which can invoke a function or a dialog box. If a null action name is supplied, the installer uses the upper-case value of the <a href="https://docs.microsoft.com/windows/desktop/Msi/action">ACTION</a> property as the action to perform. If no property value is defined, the default action is performed, defined as "INSTALL".

Actions that update the system, such as the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/installfiles-action">InstallFiles</a> and 
<a href="https://docs.microsoft.com/windows/desktop/Msi/writeregistryvalues-action">WriteRegistryValues</a> actions, cannot be run by calling 
<b>MsiDoAction</b>. The exception to this rule is if 
<b>MsiDoAction</b> is called from a custom action that is scheduled in the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/installexecutesequence-table">InstallExecuteSequence table</a> between the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/installinitialize-action">InstallInitialize</a> and 
<a href="https://docs.microsoft.com/windows/desktop/Msi/installfinalize-action">InstallFinalize actions</a>. Actions that do not update the system, such as 
<a href="https://docs.microsoft.com/windows/desktop/Msi/appsearch-action">AppSearch</a> or 
<a href="https://docs.microsoft.com/windows/desktop/Msi/costinitialize-action">CostInitialize</a>, can be called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer Action Functions</a>
 

 

