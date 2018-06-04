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

# __MIDL___MIDL_itf_gpmgmt_0000_0030_0001 enumeration


## -description


<b>GPMBackupType</b> defines the type of backup created.

<b>GPMBackupType</b> determines whether the backup is for a Group Policy object or a Starter Group Policy object.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef enum {
    typeGPO = 0,
    typeStarterGPO
} GPMBackupType;</pre>
</td>
</tr>
</table></span></div>

## -enum-fields




### -field typeGPO

Backup of a Group Policy object.


### -field typeStarterGPO

Backup of a Starter Group Policy object.

