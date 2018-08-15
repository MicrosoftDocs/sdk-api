---
UID: NF:npapi.NPCloseEnum
title: NPCloseEnum function
author: windows-sdk-content
description: Closes an enumeration.
old-location: security\npcloseenum.htm
old-project: secauthn
ms.assetid: fc6d5fe1-0953-4912-bdbd-b1372597f61d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NPCloseEnum, NPCloseEnum function [Security], _mnp_npcloseenum, npapi/NPCloseEnum, security.npcloseenum
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
 - NPCloseEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NPCloseEnum function


## -description


The <b>NPCloseEnum</b> function closes an enumeration.


## -parameters




### -param hEnum [in]

Handle obtained from an 
<a href="https://msdn.microsoft.com/d8fa7336-3ede-4445-b2e8-1a3efcae22ff">NPOpenEnum</a> call.


## -returns



If the function succeeds, it will return WN_SUCCESS. Otherwise, it will return an error code, which can be one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present. This condition is checked  before <i>hEnum</i> is tested for validity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hEnum</i> is not a valid handle.

</td>
</tr>
</table>
 



