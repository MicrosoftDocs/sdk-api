---
UID: NF:gpmgmt.IGPMSearchCriteria.Add
title: IGPMSearchCriteria::Add
author: windows-sdk-content
description: Adds a criterion for search operations.
old-location: gpmc\igpmsearchcriteria_add.htm
tech.root: GPMC
ms.assetid: 8d3f62df-6de1-4871-903f-05ac234db17f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Add, Add method [GPMC], Add method [GPMC],IGPMSearchCriteria interface, IGPMSearchCriteria interface [GPMC],Add method, IGPMSearchCriteria.Add, IGPMSearchCriteria::Add, _win32_igpmsearchcriteria_add, gpmc.igpmsearchcriteria_add, gpmgmt/IGPMSearchCriteria::Add
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMSearchCriteria.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: GPMC on Windows Vista
---

# IGPMSearchCriteria::Add


## -description


Adds a criterion for search operations.


## -parameters




### -param searchProperty [in]

The search property to evaluate. For a valid combination of search properties, search operations, and values, see the  Remarks section.


### -param searchOperation [in]

The operation to use to evaluate <i>searchProperty</i> using the value specified by <i>varValue</i>.


### -param varValue [in]

The value to evaluate <i>searchProperty</i> against.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



Following is a table that contains the valid combinations for the <i>searchProperty</i>, <i>searchOperation</i>, and <i>varValue</i> parameters.

<div class="alert"><b>Note</b>  Multiple calls to <b>IGPMSearchCriteria::Add</b> will result in a logical <b>And</b> operation of search criteria. This call does not support the <b>Or</b> logical operation functionality. Also, you can perform a <b>Not</b> of an individual criteria, but cannot perform a <b>Not</b> of a search result.</div>
<div> </div>
<table>
<tr>
<th>Search Property</th>
<th>Search Operator</th>
<th>Value</th>
</tr>
<tr>
<td>
<b>gpoPermissions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
GPMPermission

</td>
</tr>
<tr>
<td>
<b>gpoEffectivePermissions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
GPMPermission

</td>
</tr>
<tr>
<td>
<b>gpoID</b>

</td>
<td>
opEquals

opNotEquals

</td>
<td>
<b>GUID</b>

</td>
</tr>
<tr>
<td>
<b>somLinks</b>

</td>
<td>
opContains

</td>
<td>
GPMGPO

</td>
</tr>
<tr>
<td>
<b>gpoDomain</b>

</td>
<td>
opEquals

</td>
<td>
GPMDomain

</td>
</tr>
<tr>
<td>
<b>backupMostRecent</b>

</td>
<td>
opEquals

</td>
<td>
TRUE

</td>
</tr>
<tr>
<td>
<b>gpoWMIFilter</b>

</td>
<td>
opEquals

</td>
<td>
GPMWMIFilter

</td>
</tr>
<tr>
<td>
<b>backupDomain</b>

</td>
<td>
opEquals

</td>
<td>
String containing the domain name

</td>
</tr>
<tr>
<td>
<b>gpoComputerExtensions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
<b>GUID</b>

</td>
</tr>
<tr>
<td>
<b>gpoUserExtensions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
<b>GUID</b>

</td>
</tr>
<tr>
<td>
<b>gpoDisplayName</b>

</td>
<td>
opEquals

opContains

opNotContains

</td>
<td>
User-friendly GPO display name.

</td>
</tr>
<tr>
<td>
<b>starterGPOPermissions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
GPMPermission

</td>
</tr>
<tr>
<td>
<b>starterGPOEffectivePermissions</b>

</td>
<td>
opContains

opNotContains

</td>
<td>
GPMPermission

</td>
</tr>
<tr>
<td>
<b>starterGPODisplayName</b>

</td>
<td>
opEquals

opContains

opNotContains

</td>
<td>
User-friendly Starter GPO display name.

</td>
</tr>
<tr>
<td>
<b>starterGPOID</b>

</td>
<td>
opEquals

opNotEquals

</td>
<td>
<b>GUID</b>

</td>
</tr>
<tr>
<td>
<b>starterGPODomain</b>

</td>
<td>
opEquals

</td>
<td>
GPMDomain

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMDomain</a>



<a href="https://msdn.microsoft.com/6d24ffd1-987c-468f-a8cc-08992b7deb9d">IGPMSearchCriteria</a>
 

 

