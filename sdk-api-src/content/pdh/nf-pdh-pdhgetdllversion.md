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

# PdhGetDllVersion function


## -description



			Returns the version of the currently installed Pdh.dll file.
		
<div class="alert"><b>Note</b>  This function is obsolete and no longer supported.</div><div> </div>

## -parameters




### -param lpdwVersion [out]

Pointer to a variable that receives the version of Pdh.dll. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_CVERSION_WIN50"></a><a id="pdh_cversion_win50"></a><dl>
<dt><b>PDH_CVERSION_WIN50</b></dt>
</dl>
</td>
<td width="60%">
The file version is a legacy operating system.

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_VERSION"></a><a id="pdh_version"></a><dl>
<dt><b>PDH_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The file version is Windows XP.

</td>
</tr>
</table>
 


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following are possible values.




## -remarks



This function is used to help in determining the functionality that the currently installed version of Pdh.dll supports.



