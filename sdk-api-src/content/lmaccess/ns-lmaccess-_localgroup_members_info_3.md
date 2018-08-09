---
UID: NS:lmaccess._LOCALGROUP_MEMBERS_INFO_3
title: "_LOCALGROUP_MEMBERS_INFO_3"
author: windows-sdk-content
description: The LOCALGROUP_MEMBERS_INFO_3 structure contains the account name and domain name associated with a local group member.
old-location: netmgmt\localgroup_members_info_3_str.htm
old-project: netmgmt
ms.assetid: e8d1d884-c955-4706-bc3e-142469b02545
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPLOCALGROUP_MEMBERS_INFO_3, *PLOCALGROUP_MEMBERS_INFO_3, LOCALGROUP_MEMBERS_INFO_3, LOCALGROUP_MEMBERS_INFO_3 structure [Network Management], _LOCALGROUP_MEMBERS_INFO_3, _win32_localgroup_members_info_3_str, lmaccess/LOCALGROUP_MEMBERS_INFO_3, netmgmt.localgroup_members_info_3_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: LOCALGROUP_MEMBERS_INFO_3, *PLOCALGROUP_MEMBERS_INFO_3, *LPLOCALGROUP_MEMBERS_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - LOCALGROUP_MEMBERS_INFO_3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LOCALGROUP_MEMBERS_INFO_3 structure


## -description


The 
				<b>LOCALGROUP_MEMBERS_INFO_3</b> structure contains the account name and domain name associated with a local group member.


## -struct-fields




### -field lgrmi3_domainandname

Pointer to a null-terminated Unicode string specifying the account name of the local group member prefixed by the domain name and the "\" separator character. For example: 




<pre class="syntax" xml:space="preserve"><code>&lt;DomainName&gt;\&lt;AccountName&gt;
</code></pre>

## -remarks



User account names are limited to 20 characters and group names are limited to 256 characters. In addition, account names cannot be terminated by a period and they cannot include commas or any of the following printable characters: ", /, \, [, ], :, |, &lt;, &gt;, +, =, ;, ?, *. Names also cannot include characters in the range 1-31, which are nonprintable.




## -see-also




<a href="https://msdn.microsoft.com/e559cd90-942c-442a-b57f-7d2024523455">LOCALGROUP_MEMBERS_INFO_0</a>



<a href="https://msdn.microsoft.com/d6b1b729-cdd5-4ed3-a5a1-cf3a8b6cecf2">LOCALGROUP_MEMBERS_INFO_1</a>



<a href="https://msdn.microsoft.com/f5cd6e84-1111-4558-bec4-26af13f21b61">LOCALGROUP_MEMBERS_INFO_2</a>



<a href="https://msdn.microsoft.com/ed4c59d6-6532-4190-9807-95678053fc72">Local Group Functions</a>



<a href="https://msdn.microsoft.com/3b2d3e4a-742e-4e67-8b28-3cd6d7e6a857">NetLocalGroupAddMembers</a>



<a href="https://msdn.microsoft.com/85ae796b-c94a-46a8-9fa8-6c612db38671">NetLocalGroupDelMembers</a>



<a href="https://msdn.microsoft.com/35770b32-dae9-46f5-84e3-1c31ca22f708">NetLocalGroupGetMembers</a>



<a href="https://msdn.microsoft.com/4dce1e10-b74d-4d69-ac5a-12e7d9d84e5c">NetLocalGroupSetMembers</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

