---
UID: NF:msiquery.MsiSetFeatureAttributesW
title: MsiSetFeatureAttributesW function
author: windows-sdk-content
description: The MsiSetFeatureAttributes function can modify the default attributes of a feature at runtime. Note that the default attributes of features are authored in the Attributes column of the Feature table.
old-location: setup\msisetfeatureattributes.htm
tech.root: msi
ms.assetid: d8dcd6db-9792-4b34-9c78-7d11ec2d4d0f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE, INSTALLFEATUREATTRIBUTE_FAVORADVERTISE, INSTALLFEATUREATTRIBUTE_FAVORLOCAL, INSTALLFEATUREATTRIBUTE_FAVORSOURCE, INSTALLFEATUREATTRIBUTE_FOLLOWPARENT, INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE, MsiSetFeatureAttributes, MsiSetFeatureAttributes function, MsiSetFeatureAttributesA, MsiSetFeatureAttributesW, _msi_msisetfeatureattributes, msiquery/MsiSetFeatureAttributes, msiquery/MsiSetFeatureAttributesA, msiquery/MsiSetFeatureAttributesW, setup.msisetfeatureattributes
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
req.unicode-ansi: MsiSetFeatureAttributesW (Unicode) and MsiSetFeatureAttributesA (ANSI)
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
 - MsiSetFeatureAttributes
 - MsiSetFeatureAttributesA
 - MsiSetFeatureAttributesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiSetFeatureAttributesW function


## -description


The 
<b>MsiSetFeatureAttributes</b> function can modify the default attributes of a feature at runtime. Note that the default attributes of features are authored in the Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a>.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Specifies the feature name within the product.


### -param dwAttributes [in]

Feature attributes specified at run time as a set of bit flags: 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_FAVORLOCAL"></a><a id="installfeatureattribute_favorlocal"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_FAVORLOCAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesFavorLocal at run time. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_FAVORSOURCE"></a><a id="installfeatureattribute_favorsource"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_FAVORSOURCE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesFavorSource at run time. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_FOLLOWPARENT"></a><a id="installfeatureattribute_followparent"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_FOLLOWPARENT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesFollowParent at run time. Note that this is not a valid attribute to be set for top-level features. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_FAVORADVERTISE"></a><a id="installfeatureattribute_favoradvertise"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_FAVORADVERTISE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesFavorAdvertise at run time. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE"></a><a id="installfeatureattribute_disallowadvertise"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_DISALLOWADVERTISE</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesDisallowAdvertise at run time. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE"></a><a id="installfeatureattribute_nounsupportedadvertise"></a><dl>
<dt><b>INSTALLFEATUREATTRIBUTE_NOUNSUPPORTEDADVERTISE</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
Modifies default feature attributes to msidbFeatureAttributesNoUnsupportedAdvertise at run time. See Attributes column of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a> for a description.

</td>
</tr>
</table>
 


## -returns



This function returns UINT.




## -remarks



<b>MsiSetFeatureAttributes</b> must be called after 
<a href="https://msdn.microsoft.com/be9a8382-c892-44ae-8b59-c665b5cca2d2">CostInitialize action</a> and before 
<a href="https://msdn.microsoft.com/ae69ad03-5acc-4a62-ba71-3a4e477d34ab">CostFinalize action</a>. The function returns ERROR_FUNCTION_FAILED if called at any other time.

The INSTALLFEATUREATTRIBUTE_FAVORLOCAL, INSTALLFEATUREATTRIBUTE_FAVORSOURCE, and INSTALLFEATUREATTRIBUTE_FOLLOWPARENT flags are mutually exclusive. Only one of these bits can be set for any feature. If more than one of these flags is set, the behavior of that feature is undefined.

See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.



