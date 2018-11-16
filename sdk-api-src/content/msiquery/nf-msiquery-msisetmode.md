---
UID: NF:msiquery.MsiSetMode
title: MsiSetMode function
author: windows-sdk-content
description: The MsiSetMode function sets an internal engine Boolean state.
old-location: setup\msisetmode.htm
tech.root: Msi
ms.assetid: bf0eef83-8ef4-4107-b598-ccc50b179858
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MSIRUNMODE_REBOOTATEND, MSIRUNMODE_REBOOTNOW, MsiSetMode, MsiSetMode function, _msi_msisetmode, msiquery/MsiSetMode, setup.msisetmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msiquery.h
req.include-header: 
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
 - MsiSetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiSetMode
: 
---

# MsiSetMode function


## -description


The 
<b>MsiSetMode</b> function sets an internal engine Boolean state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param eRunMode [in]

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
 


### -param fState [in]

Specifies the state to set to <b>TRUE</b> or <b>FALSE</b>.


## -returns



This function returns UINT.




## -see-also




<a href="database_functions.htm">Installer State Access Functions</a>
 

 

