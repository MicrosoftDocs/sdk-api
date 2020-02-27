---
UID: NF:msiquery.MsiEvaluateConditionW
title: MsiEvaluateConditionW function (msiquery.h)
description: The MsiEvaluateCondition function evaluates a conditional expression containing property names and values.
old-location: setup\msievaluatecondition.htm
tech.root: Msi
ms.assetid: 8a444bad-8537-40ec-8c7d-6835e4319580
ms.date: 12/05/2018
ms.keywords: MsiEvaluateCondition, MsiEvaluateCondition function, MsiEvaluateConditionA, MsiEvaluateConditionW, _msi_msievaluatecondition, msiquery/MsiEvaluateCondition, msiquery/MsiEvaluateConditionA, msiquery/MsiEvaluateConditionW, setup.msievaluatecondition
f1_keywords:
- msiquery/MsiEvaluateCondition
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
req.unicode-ansi: MsiEvaluateConditionW (Unicode) and MsiEvaluateConditionA (ANSI)
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
- MsiEvaluateCondition
- MsiEvaluateConditionA
- MsiEvaluateConditionW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiEvaluateConditionW function


## -description


The 
<b>MsiEvaluateCondition</b> function evaluates a conditional expression containing property names and values.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.


### -param szCondition [in]

Specifies the conditional expression. This parameter must not be <b>NULL</b>. For the syntax of conditional expressions see 
<a href="https://docs.microsoft.com/windows/desktop/Msi/conditional-statement-syntax">Conditional Statement Syntax</a>.


## -returns



This function returns MSICONDITION.




## -remarks



The following table shows the feature and component state values used by the 
<b>MsiEvaluateCondition</b> function. These states are not set until 
<a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msisetinstalllevel">MsiSetInstallLevel</a> is called, either directly or by the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/costfinalize-action">CostFinalize action</a>. Therefore, state checking is generally only useful for conditional expressions in an action sequence table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>INSTALLSTATE_ABSENT</td>
<td>Feature or component not present.</td>
</tr>
<tr>
<td>INSTALLSTATE_LOCAL </td>
<td>Feature or component on local computer.</td>
</tr>
<tr>
<td>INSTALLSTATE_SOURCE</td>
<td>Feature or component run from source.</td>
</tr>
<tr>
<td>(null value)</td>
<td>No action to be taken on feature or component.</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Installer Action Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>
 

 

