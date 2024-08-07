---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_3
title: LOCALGROUP_MEMBERS_INFO_3 (lmaccess.h)
description: The LOCALGROUP_MEMBERS_INFO_3 structure contains the account name and domain name associated with a local group member.
helpviewer_keywords: ["*LPLOCALGROUP_MEMBERS_INFO_3","*PLOCALGROUP_MEMBERS_INFO_3","LOCALGROUP_MEMBERS_INFO_3","LOCALGROUP_MEMBERS_INFO_3 structure [Network Management]","_win32_localgroup_members_info_3_str","lmaccess/LOCALGROUP_MEMBERS_INFO_3","netmgmt.localgroup_members_info_3_str"]
old-location: netmgmt\localgroup_members_info_3_str.htm
tech.root: NetMgmt
ms.assetid: e8d1d884-c955-4706-bc3e-142469b02545
ms.date: 12/05/2018
ms.keywords: '*LPLOCALGROUP_MEMBERS_INFO_3, *PLOCALGROUP_MEMBERS_INFO_3, LOCALGROUP_MEMBERS_INFO_3, LOCALGROUP_MEMBERS_INFO_3 structure [Network Management], _win32_localgroup_members_info_3_str, lmaccess/LOCALGROUP_MEMBERS_INFO_3, netmgmt.localgroup_members_info_3_str'
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
req.typenames: LOCALGROUP_MEMBERS_INFO_3, *PLOCALGROUP_MEMBERS_INFO_3, *LPLOCALGROUP_MEMBERS_INFO_3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOCALGROUP_MEMBERS_INFO_3
 - lmaccess/_LOCALGROUP_MEMBERS_INFO_3
 - PLOCALGROUP_MEMBERS_INFO_3
 - lmaccess/PLOCALGROUP_MEMBERS_INFO_3
 - LOCALGROUP_MEMBERS_INFO_3
 - lmaccess/LOCALGROUP_MEMBERS_INFO_3
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
 - LOCALGROUP_MEMBERS_INFO_3
---

# LOCALGROUP_MEMBERS_INFO_3 structure


## -description

The 
				<b>LOCALGROUP_MEMBERS_INFO_3</b> structure contains the account name and domain name associated with a local group member.

## -struct-fields

### -field lgrmi3_domainandname

Pointer to a null-terminated Unicode string specifying the account name of the local group member prefixed by the domain name and the "\" separator character. For example: 





``` syntax
<DomainName>\<AccountName>

```


## -remarks

User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.

## -see-also

<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_0">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_1">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-localgroup_members_info_2">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="/windows/desktop/NetMgmt/local-group-functions">Local Group Functions</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmembers">NetLocalGroupAddMembers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmembers">NetLocalGroupDelMembers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupgetmembers">NetLocalGroupGetMembers</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupsetmembers">NetLocalGroupSetMembers</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
