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

# ITfInputProcessorProfileMgr::ReleaseInputProcessor


## -description


The <b>ITfInputProcessorProfileMgr::ReleaseInputProcessor</b> method deactivates the profiles belonging to the text services of the specified CLSID and releases the instance of  <a href="https://msdn.microsoft.com/fc762a6f-8d15-4082-9588-fc77fa565549">ITfTextInputProcessorEx</a> interface.


## -parameters




### -param rclsid [in]

[in] CLSID of the textservice to be released.


### -param dwFlags [in]

[in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_RIP_FLAG_FREEUNUSEDLIBRARIES"></a><a id="tf_rip_flag_freeunusedlibraries"></a><dl>
<dt><b>TF_RIP_FLAG_FREEUNUSEDLIBRARIES</b></dt>
</dl>
</td>
<td width="60%">
If this bit is on, this method calls CoFreeUnusedLibrariesEx() so the text services DLL might be freed if it does not have any more COM/DLL reference. Warning: This flag could cause some other unrelated COM/DLL free.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



