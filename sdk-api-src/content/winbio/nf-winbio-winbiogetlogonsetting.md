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

# WinBioGetLogonSetting function


## -description


Retrieves a value that indicates whether users can log on by using biometric information.


## -parameters




### -param Value [out]

Pointer to a Boolean value that specifies whether biometric logons are enabled.


### -param Source [out]

Pointer to a <b>WINBIO_SETTING_SOURCE_TYPE</b> value that specifics the setting source. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_INVALID"></a><a id="winbio_setting_source_invalid"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The setting is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_DEFAULT"></a><a id="winbio_setting_source_default"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The setting originated from built-in policy.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_LOCAL"></a><a id="winbio_setting_source_local"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
The setting originated in  the local computer registry.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_SETTING_SOURCE_POLICY"></a><a id="winbio_setting_source_policy"></a><dl>
<dt><b>WINBIO_SETTING_SOURCE_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The setting was created by Group Policy.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/57c9378d-b170-4ba8-8eee-8078531540d5">Client Application Functions</a>
 

 

