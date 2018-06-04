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

# NPFMXGetPermCaps function


## -description


Retrieves the capabilities of the permission editor. The return value is a bitmask that indicates which of the <b>Security</b> menu items in File Manager are to be enabled.


## -parameters




### -param lpDriveName [in]

Pointer to the name of the drive currently selected in File Manager.


## -returns



A bitmask that indicates what permission capability the user has on the selected drive. The bitmask is a combination of the following flags.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WNPERMC_PERM</b></dt>
</dl>
</td>
<td width="60%">
The <b>Permissions</b> menu item is enabled. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WNPERMC_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
The <b>Auditing</b> menu item is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WNPERMC_OWNER</b></dt>
</dl>
</td>
<td width="60%">
The <b>Owner</b> menu item is enabled.

</td>
</tr>
</table>
 



