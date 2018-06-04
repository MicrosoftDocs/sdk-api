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

# WerRemoveExcludedApplication function


## -description


Removes the specified application from the list of applications that are to be excluded from error reporting.


## -parameters




### -param pwzExeName [in]

A pointer to a Unicode string that specifies the name of the executable file for the application, including the file name extension. The maximum length of this path is MAX_PATH characters.

This file must have been excluded using the <a href="https://msdn.microsoft.com/ac1ec373-868f-4634-8658-4253d4f5923a">WerAddExcludedApplication</a> function or <b>WerRemoveExcludedApplication</b> fails.


### -param bAllUsers [in]

If this parameter is <b>TRUE</b>, the application name is removed from the list of excluded applications for all users. Otherwise, it is only removed from the list of excluded applications for the current user.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The process does not have access to update the list in the registry. See the Remarks section for additional information.

</td>
</tr>
</table>
 




## -remarks



This function removes applications that were added to the excluded applications list using the <a href="https://msdn.microsoft.com/ac1ec373-868f-4634-8658-4253d4f5923a">WerAddExcludedApplication</a> function.

If <i>bAllUsers</i> is <b>TRUE</b>, the list of excluded applications is stored under the HKEY_LOCAL_MACHINE registry hive. The calling process must have permissions to write to HKLM registry hive.
If <i>bAllUsers</i> is <b>FALSE</b>, the list of excluded applications is stored under the HKEY_CURRENT_USER registry hive.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/ac1ec373-868f-4634-8658-4253d4f5923a">WerAddExcludedApplication</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

