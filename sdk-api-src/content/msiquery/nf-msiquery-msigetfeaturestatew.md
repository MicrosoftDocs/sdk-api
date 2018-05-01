---
UID: NF:msiquery.MsiGetFeatureStateW
title: MsiGetFeatureStateW function
author: windows-driver-content
description: The MsiGetFeatureState function gets the requested state of a feature.
old-location: setup\msigetfeaturestate.htm
old-project: Msi
ms.assetid: eb8942b9-996e-45d8-b515-5c84737eb5ed
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: INSTALLSTATE_ABSENT, INSTALLSTATE_ADVERTISED, INSTALLSTATE_BADCONFIG, INSTALLSTATE_BROKEN, INSTALLSTATE_DEFAULT, INSTALLSTATE_INCOMPLETE, INSTALLSTATE_INVALIDARG, INSTALLSTATE_LOCAL, INSTALLSTATE_MOREDATA, INSTALLSTATE_SOURCE, INSTALLSTATE_SOURCEABSENT, INSTALLSTATE_UNKNOWN, MsiGetFeatureState, MsiGetFeatureState function, MsiGetFeatureStateA, MsiGetFeatureStateW, _msi_msigetfeaturestate, msiquery/MsiGetFeatureState, msiquery/MsiGetFeatureStateA, msiquery/MsiGetFeatureStateW, setup.msigetfeaturestate
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
req.unicode-ansi: MsiGetFeatureStateW (Unicode) and MsiGetFeatureStateA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiGetFeatureState
-	MsiGetFeatureStateA
-	MsiGetFeatureStateW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiGetFeatureStateW function


## -description


The 
<b>MsiGetFeatureState</b> function gets the requested state of a feature.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Specifies the feature name within the product.


### -param piInstalled [out]

Specifies the returned current installed state. This parameter must not be null. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_BADCONFIG"></a><a id="installstate_badconfig"></a><dl>
<dt><b>INSTALLSTATE_BADCONFIG</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_INCOMPLETE"></a><a id="installstate_incomplete"></a><dl>
<dt><b>INSTALLSTATE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The installation is suspended or in progress.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCEABSENT"></a><a id="installstate_sourceabsent"></a><dl>
<dt><b>INSTALLSTATE_SOURCEABSENT</b></dt>
</dl>
</td>
<td width="60%">
The feature must run from the source, and the source is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_MOREDATA"></a><a id="installstate_moredata"></a><dl>
<dt><b>INSTALLSTATE_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
The return buffer is full.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_INVALIDARG"></a><a id="installstate_invalidarg"></a><dl>
<dt><b>INSTALLSTATE_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_UNKNOWN"></a><a id="installstate_unknown"></a><dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unrecognized product or feature was specified.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_BROKEN"></a><a id="installstate_broken"></a><dl>
<dt><b>INSTALLSTATE_BROKEN</b></dt>
</dl>
</td>
<td width="60%">
The feature is broken.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ADVERTISED"></a><a id="installstate_advertised"></a><dl>
<dt><b>INSTALLSTATE_ADVERTISED</b></dt>
</dl>
</td>
<td width="60%">
The advertised feature.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The feature was uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The feature was installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The feature must run from the source, CD-ROM, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The feature is  installed in the default location: local or source.

</td>
</tr>
</table>
 


### -param piAction [out]

Receives the action taken during the installation session. This parameter must not be null. For return values, see <i>piInstalled</i>.


## -returns




					The 
<b>MsiGetFeatureState</b> function returns the following values:




## -remarks



See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Installer Selection Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

