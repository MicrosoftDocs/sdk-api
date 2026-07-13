---
UID: NF:npapi.NPCloseEnum
title: NPCloseEnum function (npapi.h)
description: Closes an enumeration.
helpviewer_keywords: ["NPCloseEnum","NPCloseEnum function [Security]","_mnp_npcloseenum","npapi/NPCloseEnum","security.npcloseenum"]
old-location: security\npcloseenum.htm
tech.root: security
ms.assetid: fc6d5fe1-0953-4912-bdbd-b1372597f61d
ms.date: 12/05/2018
ms.keywords: NPCloseEnum, NPCloseEnum function [Security], _mnp_npcloseenum, npapi/NPCloseEnum, security.npcloseenum
req.header: npapi.h
req.include-header: 
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
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPCloseEnum
 - npapi/NPCloseEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPCloseEnum
---

# NPCloseEnum function


## -description

The <b>NPCloseEnum</b> function closes an enumeration.

## -parameters

### -param hEnum [in]

Handle obtained from an 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a> call.

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