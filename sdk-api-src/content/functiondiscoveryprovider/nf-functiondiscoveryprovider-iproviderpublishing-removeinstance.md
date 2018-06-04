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

# IProviderPublishing::RemoveInstance


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes an existing function instance.


## -parameters




### -param enumVisibilityFlags [in]

A <a href="https://msdn.microsoft.com/a3388293-150c-417a-a4a6-0d5020e0ae82">SystemVisibilityFlags</a> enumeration value which specifies the visibility of the function instance which the provider is about to delete.  It is up to the provider whether or not to honor this setting, however the current user visibility can be used to allow processes running in a non-Administrator security context to still be able to remove function instances.


### -param pszSubCategory [in]

The subcategory string of the function instance.


### -param pszProviderInstanceIdentity [in]

The provider instance identifier.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSiteInfo</i>, <i>pszSubCategory</i>, or <i>pszProviderInstanceIdentity</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7647db1b-88c8-44f3-b2af-a61dad4790f6">IProviderPublishing</a>
 

 

