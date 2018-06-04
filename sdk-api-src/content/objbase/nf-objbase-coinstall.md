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

# CoInstall function


## -description


Installs the requested COM server application. 


## -parameters




### -param pbc [in]

This parameter is reserved and must be <b>NULL</b>.


### -param dwFlags [in]

This parameter is reserved and must be 0.


### -param pClassSpec [in]

A pointer to a uCLSSPEC structure. The <b>tyspec</b> member must be set to TYSPEC_CLSID and the <b>clsid</b> member must be set to the CLSID to be installed. For more information see <a href="https://msdn.microsoft.com/f2972300-5a95-43e3-b2d1-cd8f30d14d1d">TYSPEC</a>.


### -param pQuery [in]

A pointer to a <a href="https://msdn.microsoft.com/5d6a17e1-dcdd-4691-aec2-f63dbcb26027">QUERYCONTEXT</a> structure. The <b>dwContext</b> member must be set to the desired <a href="https://msdn.microsoft.com/dcb82ff2-56e4-4c7e-a621-7ffd0f1a9d8e">CLSCTX</a> value.


### -param pszCodeBase [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This function can return the standard return value E_INVALIDARG, as well as the following values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CS_E_PACKAGE_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>tyspec</b> member of <i>pClassSpec</i> was not set to TYSPEC_CLSID.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5d6a17e1-dcdd-4691-aec2-f63dbcb26027">QUERYCONTEXT</a>



<a href="https://msdn.microsoft.com/f2972300-5a95-43e3-b2d1-cd8f30d14d1d">TYSPEC</a>
 

 

