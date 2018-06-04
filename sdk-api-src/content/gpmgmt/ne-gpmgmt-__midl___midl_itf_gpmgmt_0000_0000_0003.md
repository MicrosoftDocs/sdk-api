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

# __MIDL___MIDL_itf_gpmgmt_0000_0000_0003 enumeration


## -description


<b>GPMSearchProperty</b> defines  the property of the search criteria.

The property of the search criteria.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef enum {gpoPermissions, gpoEffectivePermissions, gpoDisplayName, gpoWMIFilter, gpoID, 
              gpoComputerExtensions, gpoUserExtensions, somLinks, gpoDomain, backupMostRecent,
              starterGPOPermissions, starterGPOEffectivePermissions, starterGPODisplayName, starterGPOID,
              starterGPODomain} GPMSearchProperty;</pre>
</td>
</tr>
</table></span></div>

## -enum-fields




### -field gpoPermissions

The specified level of permission for a Group Policy Object.


### -field gpoEffectivePermissions

A specific set of permissions, whether the permissions are explicitly set or derived as a result of group membership.


### -field gpoDisplayName

Display name of a Group Policy object.


### -field gpoWMIFilter

Display name of a WMI filter.


### -field gpoID

GUID of a Group Policy object.


### -field gpoComputerExtensions

Computer client-side extension


### -field gpoUserExtensions

user client-side extension


### -field somLinks

Scope of Management (SOM) that link to a Group Policy object.


### -field gpoDomain

domain name


### -field backupMostRecent

The most recent backup


### -field starterGPOPermissions

The specified level of permission for a Starter Group Policy Object.


### -field starterGPOEffectivePermissions

A specific set of permissions, whether the permissions are explicitly set or derived as a result of group membership.


### -field starterGPODisplayName

Display name of a Starter Group Policy object.


### -field starterGPOID

GUID of a Starter Group Policy object.


### -field starterGPODomain

domain name

