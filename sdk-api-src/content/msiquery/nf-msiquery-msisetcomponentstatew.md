---
UID: NF:msiquery.MsiSetComponentStateW
title: MsiSetComponentStateW function
author: windows-sdk-content
description: The MsiSetComponentState function sets a component to the requested state.
old-location: setup\msisetcomponentstate.htm
old-project: msi
ms.assetid: d538c81f-130b-4522-9f85-47f04e24f125
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiSetComponentState, MsiSetComponentState function, MsiSetComponentStateA, MsiSetComponentStateW, _msi_msisetcomponentstate, msiquery/MsiSetComponentState, msiquery/MsiSetComponentStateA, msiquery/MsiSetComponentStateW, setup.msisetcomponentstate
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
req.unicode-ansi: MsiSetComponentStateW (Unicode) and MsiSetComponentStateA (ANSI)
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
 - MsiSetComponentState
 - MsiSetComponentStateA
 - MsiSetComponentStateW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiSetComponentStateW function


## -description


The 
<b>MsiSetComponentState</b> function sets a component to the requested state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szComponent [in]

Specifies the name of the component.


### -param iState [in]

Specifies the state to set. This parameter can be one of the following values. 



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
The component was uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The component was installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The component will run from source, CD, or network.

</td>
</tr>
</table>
 


## -returns



The 
<b>MsiSetComponentState</b> function returns the following values:
					




## -remarks



The 
<b>MsiSetComponentState</b> function requests a change in the Action state of a record in the 
<a href="https://msdn.microsoft.com/069d64e9-106a-42b7-8dea-a44fc0c6e0cd">Component table</a>.

For more information, see 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Installer Selection Functions</a>
 

 

