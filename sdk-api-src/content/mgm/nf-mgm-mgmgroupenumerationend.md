---
UID: NF:mgm.MgmGroupEnumerationEnd
title: MgmGroupEnumerationEnd function (mgm.h)
description: The MgmGroupEnumerationEnd function releases the specified enumeration handle that was obtained from a previous call to MgmGroupEnumerationStart.
helpviewer_keywords: ["MgmGroupEnumerationEnd","MgmGroupEnumerationEnd function [RAS]","_mpr_mgmgroupenumerationend","mgm/MgmGroupEnumerationEnd","rras.mgmgroupenumerationend"]
old-location: rras\mgmgroupenumerationend.htm
tech.root: RRAS
ms.assetid: 87a0bd96-c877-443e-a539-a31ab0971869
ms.date: 12/05/2018
ms.keywords: MgmGroupEnumerationEnd, MgmGroupEnumerationEnd function [RAS], _mpr_mgmgroupenumerationend, mgm/MgmGroupEnumerationEnd, rras.mgmgroupenumerationend
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MgmGroupEnumerationEnd
 - mgm/MgmGroupEnumerationEnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - MgmGroupEnumerationEnd
---

# MgmGroupEnumerationEnd function


## -description

The 
<b>MgmGroupEnumerationEnd</b> function releases the specified enumeration handle that was obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>.

## -parameters

### -param hEnum [in]

Specifies the enumeration handle to release.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Could not complete the call to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid enumeration handle.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>