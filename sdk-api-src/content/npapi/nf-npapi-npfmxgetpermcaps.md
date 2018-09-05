---
UID: NF:npapi.NPFMXGetPermCaps
title: NPFMXGetPermCaps function
author: windows-sdk-content
description: Retrieves the capabilities of the permission editor. The return value is a bitmask that indicates which of the Security menu items in File Manager are to be enabled.
old-location: security\npfmxgetpermcaps.htm
old-project: SecAuthN
ms.assetid: 1df2c1d4-ce70-494d-98e4-cda553403215
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NPFMXGetPermCaps, NPFMXGetPermCaps function [Security], _mnp_npfmxgetpermcaps, npapi/NPFMXGetPermCaps, security.npfmxgetpermcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: npapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NOTIFICATION_USER_INPUT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPFMXGetPermCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 



