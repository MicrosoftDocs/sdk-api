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

# MsiSetMode function


## -description


The 
<b>MsiSetMode</b> function sets an internal engine Boolean state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param eRunMode

TBD


### -param fState [in]

Specifies the state to set to <b>TRUE</b> or <b>FALSE</b>.


#### - iRunMode [in]

Specifies the run mode. This parameter must be one of the following values. While there are many values for this parameter, as described in 
<a href="https://msdn.microsoft.com/45827df5-3f3f-4fb9-bdfe-38dc78a45321">MsiGetMode</a>, only one of the following values can be set. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTATEND"></a><a id="msirunmode_rebootatend"></a><dl>
<dt><b>MSIRUNMODE_REBOOTATEND</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary after a successful installation.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIRUNMODE_REBOOTNOW"></a><a id="msirunmode_rebootnow"></a><dl>
<dt><b>MSIRUNMODE_REBOOTNOW</b></dt>
</dl>
</td>
<td width="60%">
A reboot is necessary to continue installation.

</td>
</tr>
</table>
 


## -returns



This function returns UINT.




## -see-also




<a href="database_functions.htm">Installer State Access Functions</a>
 

 

