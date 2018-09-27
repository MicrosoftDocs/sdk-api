---
UID: NF:msiquery.MsiGetComponentStateW
title: MsiGetComponentStateW function
author: windows-sdk-content
description: The MsiGetComponentState function obtains the state of a component.
old-location: setup\msigetcomponentstate.htm
tech.root: msi
ms.assetid: 343f5cbc-e026-4a51-9c54-da5d10b7caa8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_DEFAULT, INSTALLSTATE_LOCAL, INSTALLSTATE_REMOVED, INSTALLSTATE_SOURCE, INSTALLSTATE_UNKNOWN, MsiGetComponentState, MsiGetComponentState function, MsiGetComponentStateA, MsiGetComponentStateW, _msi_msigetcomponentstate, msiquery/MsiGetComponentState, msiquery/MsiGetComponentStateA, msiquery/MsiGetComponentStateW, setup.msigetcomponentstate
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
req.unicode-ansi: MsiGetComponentStateW (Unicode) and MsiGetComponentStateA (ANSI)
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
 - MsiGetComponentState
 - MsiGetComponentStateA
 - MsiGetComponentStateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiGetComponentStateW function


## -description


The 
<b>MsiGetComponentState</b> function obtains the state of a component.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szComponent [in]

A null-terminated string that specifies the component name within the product.


### -param piInstalled [out]

Receives the current installed state. This parameter must not be null. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The component is not installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The component is installed in the default location: local or source.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component is installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_REMOVED"></a><a id="installstate_removed"></a><dl>
<dt><b>INSTALLSTATE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
The component is being removed. In action state and not settable.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component runs from the source, CD-ROM, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_UNKNOWN"></a><a id="installstate_unknown"></a><dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unrecognized product or feature name was passed to the function.

</td>
</tr>
</table>
 


### -param piAction [out]

Receives the action taken during the installation. This parameter must not be null. For return values, see <i>piInstalled</i>.


## -returns



The 
<b>MsiGetComponentState</b> function returns the following values:




## -remarks



If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.

For more information, see 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer Selection Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

