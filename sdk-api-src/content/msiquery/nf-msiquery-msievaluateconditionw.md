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

# MsiEvaluateConditionW function


## -description


The 
<b>MsiEvaluateCondition</b> function evaluates a conditional expression containing property names and values.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szCondition [in]

Specifies the conditional expression. This parameter must not be <b>NULL</b>. For the syntax of conditional expressions see 
<a href="https://msdn.microsoft.com/6f1657f9-063b-4d57-ad76-95e3dbe25786">Conditional Statement Syntax</a>.


## -returns



This function returns MSICONDITION.




## -remarks



The following table shows the feature and component state values used by the 
<b>MsiEvaluateCondition</b> function. These states are not set until 
<a href="https://msdn.microsoft.com/98f1d91d-632e-4dea-948f-2dc416b4d410">MsiSetInstallLevel</a> is called, either directly or by the 
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize action</a>. Therefore, state checking is generally only useful for conditional expressions in an action sequence table.

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




<a href="database_functions.htm">Installer Action Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

