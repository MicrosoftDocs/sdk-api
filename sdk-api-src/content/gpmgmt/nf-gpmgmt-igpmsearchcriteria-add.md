---
UID: NF:gpmgmt.IGPMSearchCriteria.Add
title: IGPMSearchCriteria::Add (gpmgmt.h)
description: Adds a criterion for search operations.
helpviewer_keywords: ["Add","Add method [GPMC]","Add method [GPMC]","IGPMSearchCriteria interface","IGPMSearchCriteria interface [GPMC]","Add method","IGPMSearchCriteria.Add","IGPMSearchCriteria::Add","_win32_igpmsearchcriteria_add","gpmc.igpmsearchcriteria_add","gpmgmt/IGPMSearchCriteria::Add"]
old-location: gpmc\igpmsearchcriteria_add.htm
tech.root: gpmc
ms.assetid: 8d3f62df-6de1-4871-903f-05ac234db17f
ms.date: 12/05/2018
ms.keywords: Add, Add method [GPMC], Add method [GPMC],IGPMSearchCriteria interface, IGPMSearchCriteria interface [GPMC],Add method, IGPMSearchCriteria.Add, IGPMSearchCriteria::Add, _win32_igpmsearchcriteria_add, gpmc.igpmsearchcriteria_add, gpmgmt/IGPMSearchCriteria::Add
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
targetos: Windows
req.typenames: 
req.redist: GPMC on Windows Vista
ms.custom: 19H1
f1_keywords:
 - IGPMSearchCriteria::Add
 - gpmgmt/IGPMSearchCriteria::Add
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMSearchCriteria.Add
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

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a>