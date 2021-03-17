---
UID: NF:mgm.MgmGroupEnumerationStart
title: MgmGroupEnumerationStart function (mgm.h)
description: The MgmGroupEnumerationStart function obtains an enumeration handle that is later used to obtain the list of groups that have been joined. After the client obtains the handle, it should use the MgmGroupEnumerationGetNext function to enumerate the groups.
helpviewer_keywords: ["ALL_SOURCES","ANY_SOURCE","MgmGroupEnumerationStart","MgmGroupEnumerationStart function [RAS]","_mpr_mgmgroupenumerationstart","mgm/MgmGroupEnumerationStart","rras.mgmgroupenumerationstart"]
old-location: rras\mgmgroupenumerationstart.htm
tech.root: RRAS
ms.assetid: 926f4055-becb-4c99-afd2-2d2822626f24
ms.date: 12/05/2018
ms.keywords: ALL_SOURCES, ANY_SOURCE, MgmGroupEnumerationStart, MgmGroupEnumerationStart function [RAS], _mpr_mgmgroupenumerationstart, mgm/MgmGroupEnumerationStart, rras.mgmgroupenumerationstart
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
 - MgmGroupEnumerationStart
 - mgm/MgmGroupEnumerationStart
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
 - MgmGroupEnumerationStart
---

# MgmGroupEnumerationStart function


## -description

The 
<b>MgmGroupEnumerationStart</b> function obtains an enumeration handle that is later used to obtain the list of groups that have been joined. After the client obtains the handle, it should use the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a> function to enumerate the groups.

## -parameters

### -param hProtocol [in]

Handle to the protocol obtained from a previous call to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmregistermprotocol">MgmRegisterMProtocol</a>.

### -param metEnumType [in]

Specifies the type of enumeration. The following enumerations are available. 



<table>
<tr>
<th>Enumeration</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALL_SOURCES"></a><a id="all_sources"></a><dl>
<dt><b>ALL_SOURCES</b></dt>
</dl>
</td>
<td width="60%">
Retrieves wildcard joins (*, g) and source-specific joins (s, g).

</td>
</tr>
<tr>
<td width="40%"><a id="ANY_SOURCE"></a><a id="any_source"></a><dl>
<dt><b>ANY_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves group entries that have at least one source specified.

</td>
</tr>
</table>

### -param phEnumHandle [out]

Receives the handle to the enumeration. Use this handle in calls to 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a> and 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationend">MgmGroupEnumerationEnd</a>.

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
Invalid handle to a protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/mgm/ne-mgm-mgm_enum_types">MGM_ENUM_TYPES</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationend">MgmGroupEnumerationEnd</a>



<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationgetnext">MgmGroupEnumerationGetNext</a>