---
UID: NF:msiquery.MsiSetFeatureStateW
title: MsiSetFeatureStateW function (msiquery.h)
author: windows-sdk-content
description: The MsiSetFeatureState function sets a feature to a specified state.
old-location: setup\msisetfeaturestate.htm
tech.root: Msi
ms.assetid: c7b22484-5a89-44f2-b0ff-6061a7fc5703
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_LOCAL, INSTALLSTATE_SOURCE, MsiSetFeatureState, MsiSetFeatureState function, MsiSetFeatureStateA, MsiSetFeatureStateW, _msi_msisetfeaturestate, msiquery/MsiSetFeatureState, msiquery/MsiSetFeatureStateA, msiquery/MsiSetFeatureStateW, setup.msisetfeaturestate
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiSetFeatureStateW (Unicode) and MsiSetFeatureStateA (ANSI)
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
 - MsiSetFeatureState
 - MsiSetFeatureStateA
 - MsiSetFeatureStateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiSetFeatureStateW function


## -description


The 
<b>MsiSetFeatureState</b> function sets a feature to a specified state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Specifies the name of the feature.


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
The feature is not installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature is installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature is run from the source, CD, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The feature is advertised.

</td>
</tr>
</table>
 


## -returns



The 
<b>MsiSetFeatureState</b> function returns the following values:




## -remarks



The 
<b>MsiSetFeatureState</b> function requests a change in the select state of a feature in the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature</a> table and its children. In turn, the action state of all the components linked to the changed feature records are also updated appropriately, based on the new feature select state.

The 
<a href="https://msdn.microsoft.com/98f1d91d-632e-4dea-948f-2dc416b4d410">MsiSetInstallLevel</a> function must be called before calling 
<b>MsiSetFeatureState</b>.

When <b>MsiSetFeatureState</b> is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state. However, there are common situations when the request cannot be fully implemented. For example, if a feature is tied to two components, component A and component B, through the <a href="https://msdn.microsoft.com/aff16483-a9ed-4675-8e87-8adf695605ee">FeatureComponents</a> table, and component A has the <b>msidbComponentAttributesLocalOnly</b> attribute and component B has the <b>msidbComponentAttributesSourceOnly</b> attribute. In this case, if <b>MsiSetFeatureState</b> is called with a requested state of either INSTALLSTATE_LOCAL or INSTALLSTATE_SOURCE, the request cannot be fully implemented for both components. In this case, both components are turned ON, with component A set to Local and component B set to Source.

If more than one feature is linked to a single component (a common scenario), the final action state of that component is determined as follows:

<ul>
<li>If at least one feature requires the component to be installed locally, the feature is installed with a state of local.</li>
<li>If at least one feature requires the component to be run from the source, the feature is installed with a state of source.</li>
<li>If at least one feature requires the removal of the component, the action state is absent.</li>
</ul>
See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions from Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer Selection Functions</a>
 

 

