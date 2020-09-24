---
UID: NS:lmaccess._NET_DISPLAY_GROUP
title: NET_DISPLAY_GROUP (lmaccess.h)
description: The NET_DISPLAY_GROUP structure contains information that an account manager can access to determine information about group accounts.
helpviewer_keywords: ["*PNET_DISPLAY_GROUP","NET_DISPLAY_GROUP","NET_DISPLAY_GROUP structure [Network Management]","PNET_DISPLAY_GROUP","PNET_DISPLAY_GROUP structure pointer [Network Management]","_win32_net_display_group_str","lmaccess/NET_DISPLAY_GROUP","lmaccess/PNET_DISPLAY_GROUP","netmgmt.net_display_group_str"]
old-location: netmgmt\net_display_group_str.htm
tech.root: NetMgmt
ms.assetid: 8e467f20-2cfb-40ae-a8b2-a5350d736eed
ms.date: 12/05/2018
ms.keywords: '*PNET_DISPLAY_GROUP, NET_DISPLAY_GROUP, NET_DISPLAY_GROUP structure [Network Management], PNET_DISPLAY_GROUP, PNET_DISPLAY_GROUP structure pointer [Network Management], _win32_net_display_group_str, lmaccess/NET_DISPLAY_GROUP, lmaccess/PNET_DISPLAY_GROUP, netmgmt.net_display_group_str'
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NET_DISPLAY_GROUP, *PNET_DISPLAY_GROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_DISPLAY_GROUP
 - lmaccess/_NET_DISPLAY_GROUP
 - PNET_DISPLAY_GROUP
 - lmaccess/PNET_DISPLAY_GROUP
 - NET_DISPLAY_GROUP
 - lmaccess/NET_DISPLAY_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - NET_DISPLAY_GROUP
---

# NET_DISPLAY_GROUP structure


## -description

The
				<b>NET_DISPLAY_GROUP</b> structure contains information that an account manager can access to determine information about group accounts.

## -struct-fields

### -field grpi3_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of the group.

### -field grpi3_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains a comment associated with the group. This string can be a null string, or it can have any number of characters before the terminating null character.

### -field grpi3_group_id

Type: <b>DWORD</b>

The relative identifier (RID) of the group. The relative identifier is determined by the accounts database when the group is created. It uniquely identifies the group to the account manager within the domain. The 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a> functions ignore this member. For more information about RIDs, see 
<a href="/windows/desktop/SecAuthZ/sid-components">SID Components</a>.

### -field grpi3_attributes

Type: <b>DWORD</b>

These attributes are hard-coded to SE_GROUP_MANDATORY, SE_GROUP_ENABLED, and SE_GROUP_ENABLED_BY_DEFAULT. For more information, see 
<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>.

### -field grpi3_next_index

Type: <b>DWORD</b>

The index of the last entry returned by the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a> function. Pass this value as the <i>Index</i> parameter to 
<b>NetQueryDisplayInformation</b> to return the next logical entry. Note that you should not use the value of this member for any purpose except to retrieve more data with additional calls to 
<b>NetQueryDisplayInformation</b>.

## -see-also

<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd">NetUserAdd</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo">NetUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>