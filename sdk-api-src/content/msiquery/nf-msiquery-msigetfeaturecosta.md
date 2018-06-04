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

# MsiGetFeatureCostA function


## -description


The 
<b>MsiGetFeatureCost</b> function returns the disk space required by a feature and its selected children and parent features.


## -parameters




### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a>, <a href="https://msdn.microsoft.com/9e9550e9-9c10-4ef1-a172-dfacaaa37fd0">MsiOpenPackageEx</a>, or <a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a>.


### -param szFeature [in]

Specifies the name of the feature.


### -param iCostTree [in]

Specifies the value the function uses to determine disk space requirements. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSICOSTTREE_CHILDREN"></a><a id="msicosttree_children"></a><dl>
<dt><b>MSICOSTTREE_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
The children of the indicated feature are included in the cost.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICOSTTREE_PARENTS"></a><a id="msicosttree_parents"></a><dl>
<dt><b>MSICOSTTREE_PARENTS</b></dt>
</dl>
</td>
<td width="60%">
The parent features of the indicated feature are included in the cost.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICOSTTREE_SELFONLY"></a><a id="msicosttree_selfonly"></a><dl>
<dt><b>MSICOSTTREE_SELFONLY</b></dt>
</dl>
</td>
<td width="60%">
The feature only is included in the cost.

</td>
</tr>
</table>
 


### -param iState [in]

Specifies the installation state. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_UNKNOWN"></a><a id="installstate_unknown"></a><dl>
<dt><b>INSTALLSTATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The product or feature is unrecognized.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_ABSENT"></a><a id="installstate_absent"></a><dl>
<dt><b>INSTALLSTATE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The product or feature is uninstalled.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_LOCAL"></a><a id="installstate_local"></a><dl>
<dt><b>INSTALLSTATE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The product or feature is installed on the local drive.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_SOURCE"></a><a id="installstate_source"></a><dl>
<dt><b>INSTALLSTATE_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The product or feature is installed to run from source, CD, or network.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLSTATE_DEFAULT"></a><a id="installstate_default"></a><dl>
<dt><b>INSTALLSTATE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The product or feature will be installed to use the default location: local or source.

</td>
</tr>
</table>
 


### -param piCost [out]

Receives the disk space requirements in units of 512 bytes. This parameter must not be null.


## -returns



The 
<b>MsiGetFeatureCost</b> function returns the following values:
					




## -remarks



See 
<a href="https://msdn.microsoft.com/b9795825-41fa-474b-a0c5-06770aa99bc1">Calling Database Functions From Programs</a>.

With the 
<b>MsiGetFeatureCost</b> function, the MSICOSTTREE_SELFONLY value indicates the total amount of disk space (in units of 512 bytes) required by the specified feature only. This returned value does not include the children or the parent features of the specified feature. This total cost is made up of the disk costs attributed to every component linked to the feature.

The MSICOSTTREE_CHILDREN value indicates the total amount of disk space (in units of 512 bytes) required by the specified feature and its children. For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.

The MSICOSTTREE_PARENTS value indicates the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the 
<a href="https://msdn.microsoft.com/1faee1d5-6e39-43ea-bf92-a0b3986a13a1">Feature table</a>). For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.

<b>MsiGetFeatureCost</b> is dependent upon several other functions to be successful. The following example demonstrates the order in which these functions must be called:

<pre class="syntax" xml:space="preserve"><code>MSIHANDLE   hInstall;      //product handle, must be closed
int         iCost;         //cost returned by MsiGetFeatureCost

MsiOpenPackage("Path to package....",&amp;hInstall);   //"Path to package...." should be replaced with the full path to the package to be opened
MsiDoAction(hInstall,"CostInitialize");         //
MsiDoAction(hInstall,"FileCost");
MsiDoAction(hInstall,"CostFinalize");
MsiDoAction(hInstall,"InstallValidate");
MsiGetFeatureCost(hInstall,"FeatureName",MSICOSTTREE_SELFONLY,INSTALLSTATE_ABSENT,&amp;iCost);
MsiCloseHandle(hInstall);                        //close the open product handle</code></pre>
The process to query the cost of features scheduled to be removed is slightly different:

<pre class="syntax" xml:space="preserve"><code>MSIHANDLE   hInstall;      //product handle, must be closed
int         iCost;         //cost returned by MsiGetFeatureCost

MsiOpenPackage("Path to package....",&amp;hInstall);              //"Path to package...." should be replaced with the full path to the package to be opened
MsiDoAction(hInstall,"CostInitialize");                          //
MsiDoAction(hInstall,"FileCost");
MsiDoAction(hInstall,"CostFinalize");
MsiSetFeatureState(hInstall,"FeatureName",INSTALLSTATE_ABSENT);  //set the feature's state to "not installed"
MsiDoAction(hInstall,"InstallValidate");
MsiGetFeatureCost(hInstall,"FeatureName",MSICOSTTREE_SELFONLY,INSTALLSTATE_ABSENT,&amp;iCost);
MsiCloseHandle(hInstall);                                        //close the open product handle</code></pre>
If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Installer Selection Functions</a>



<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>
 

 

