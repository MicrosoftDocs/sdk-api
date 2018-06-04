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

# IAssemblyCacheItem::Commit


## -description


The <b>Commit</b> method copies information into the side-by-side store. When this method returns, the assembly is visible in the side-by-side store.


## -parameters




### -param dwFlags [in]

This parameter specifies how existing information in the side-by-side store is to be replaced by information for the assembly being installed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH"></a><a id="iassemblycacheitem_commit_flag_refresh"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_FLAG_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing information in the side-by-side store with the information in the assembly being installed if the version in the assembly is greater than or equal to the version of the existing information. This is the default option.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH"></a><a id="iassemblycacheitem_commit_flag_force_refresh"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_FLAG_FORCE_REFRESH</b></dt>
</dl>
</td>
<td width="60%">
Replace existing information in the side-by-side store with the information for the assembly being installed.

</td>
</tr>
</table>
 


### -param pulDisposition [out, optional]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED"></a><a id="iassemblycacheitem_commit_disposition_installed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly is installed for the first time.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED"></a><a id="iassemblycacheitem_commit_disposition_refreshed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_REFRESHED</b></dt>
</dl>
</td>
<td width="60%">
The assembly replaces an existing assembly.

</td>
</tr>
<tr>
<td width="40%"><a id="IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED"></a><a id="iassemblycacheitem_commit_disposition_already_installed"></a><dl>
<dt><b>IASSEMBLYCACHEITEM_COMMIT_DISPOSITION_ALREADY_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The assembly is already installed in the side-by-side assembly store.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The method did not succeed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9df9ee58-0354-49f0-af9c-5b92179cfaea">IAssemblyCacheItem</a>
 

 

