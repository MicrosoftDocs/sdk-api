---
UID: NF:msiquery.MsiGetFeatureValidStatesW
title: MsiGetFeatureValidStatesW function
author: windows-sdk-content
description: The MsiGetFeatureValidStates function returns a valid installation state.
old-location: setup\msigetfeaturevalidstates.htm
tech.root: MSI
ms.assetid: c4c3f484-6854-4019-9dc0-e4c99162c339
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 16, 2, 32, 4, 8, MsiGetFeatureValidStates, MsiGetFeatureValidStates function, MsiGetFeatureValidStatesA, MsiGetFeatureValidStatesW, _msi_msigetfeaturevalidstates, msiquery/MsiGetFeatureValidStates, msiquery/MsiGetFeatureValidStatesA, msiquery/MsiGetFeatureValidStatesW, setup.msigetfeaturevalidstates
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
req.unicode-ansi: MsiGetFeatureValidStatesW (Unicode) and MsiGetFeatureValidStatesA (ANSI)
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
 - MsiGetFeatureValidStates
 - MsiGetFeatureValidStatesA
 - MsiGetFeatureValidStatesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiGetFeatureValidStatesW function


## -description


The 
<b>MsiGetFeatureValidStates</b> function returns a valid installation state.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Specifies the feature name.


### -param lpInstallStates [out]

Receives the location to hold the valid installation states. For each valid installation state, the installer sets <i>pInstallState</i> to a combination of the following values. This parameter should not be null.

<table>
<tr>
<th>Decimal Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>INSTALLSTATE_ADVERTISED</dt>
</dl>
</td>
<td width="60%">
The feature can be advertised.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
<dt>INSTALLSTATE_ABSENT</dt>
</dl>
</td>
<td width="60%">
The feature can be absent.

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
<dt>INSTALLSTATE_LOCAL</dt>
</dl>
</td>
<td width="60%">
The feature can be installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="16"></a><dl>
<dt><b>16</b></dt>
<dt>INSTALLSTATE_SOURCE</dt>
</dl>
</td>
<td width="60%">
The feature can be configured to run from source, CD-ROM, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="32"></a><dl>
<dt><b>32</b></dt>
<dt>INSTALLSTATE_DEFAULT</dt>
</dl>
</td>
<td width="60%">
The feature can be configured to use the default location: local or source.

</td>
</tr>
</table>
 


## -returns



The 
<b>MsiGetFeatureValidStates</b> function returns the following values:




## -remarks



See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

The <b>MsiGetFeatureValidStates</b> function determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.  

The possible valid states for a feature are determined as follows:

<ul>
<li>If the feature does not contain components, both INSTALLSTATE_LOCAL and INSTALLSTATE_SOURCE are valid states for the feature.</li>
<li>If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE_LOCAL is a valid state for the feature.</li>
<li>If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE_SOURCE is a valid state for the feature.</li>
<li>If a file of a component that belongs to the feature is patched or from a compressed source, then INSTALLSTATE_SOURCE is not included as a valid state for the feature.</li>
<li>INSTALLSTATE_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</li>
<li>INSTALLSTATE_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</li>
<li>Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</li>
</ul>
After calling 
<b>MsiGetFeatureValidStates</b> a conditional statement may then be used to test the valid installation states of a feature. For example, the following call to 
<b>MsiGetFeatureValidStates</b> gets the installation state of Feature1.

<pre class="syntax" xml:space="preserve"><code>MsiGetFeatureValidStates(hProduct, "Feature1", &amp;dwValidStates);</code></pre>
If Feature1 has attributes of value 0 (favor local), and Feature1 has one component with attributes of value 0 (local only), the value of dwValidStates after the call is 14. This indicates that INSTALLSTATE_LOCAL, INSTALLSTATE_ABSENT,and INSTALLSTATE_ADVERTISED are valid states for Feature1. The following conditional statement evaluates to True if local is a valid state for this feature.

( ( dwValidStates &amp; ( 1 &lt;&lt; INSTALLSTATE_LOCAL ) ) == ( 1 &lt;&lt; INSTALLSTATE_LOCAL ) )

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Installer Selection Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

