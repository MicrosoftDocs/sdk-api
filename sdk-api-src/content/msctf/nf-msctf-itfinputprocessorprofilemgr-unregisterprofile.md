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

# ITfInputProcessorProfileMgr::UnregisterProfile


## -description


The <b>ITfInputProcessorProfileMgr::UnregisterProfile</b> method unregisters the text service and the profile.


## -parameters




### -param rclsid [in]

[in] CLSID of the text service.


### -param langid [in]

[in] The language id of the profile.


### -param guidProfile [in]

[in] The GUID to identify the profile.


### -param dwFlags [in]

[in] The combination of the following bits:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_URP_ALLPROFILES"></a><a id="tf_urp_allprofiles"></a><dl>
<dt><b>TF_URP_ALLPROFILES</b></dt>
</dl>
</td>
<td width="60%">
If this bit is on, <b>UnregistrProfile</b> unregisters all profiles of the <i>rclsid</i> parameter. The <i>langid</i> and <i>guidProfile</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_URP_LOCALPROCESS"></a><a id="tf_urp_localprocess"></a><dl>
<dt><b>TF_URP_LOCALPROCESS</b></dt>
</dl>
</td>
<td width="60%">
The profile was registered on the local process.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_URP_LOCALTHREAD"></a><a id="tf_urp_localthread"></a><dl>
<dt><b>TF_URP_LOCALTHREAD</b></dt>
</dl>
</td>
<td width="60%">
The profile was registered on the local thread.

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
 



