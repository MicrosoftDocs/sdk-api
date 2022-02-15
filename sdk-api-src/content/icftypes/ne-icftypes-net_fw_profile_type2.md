---
UID: NE:icftypes.NET_FW_PROFILE_TYPE2_
title: NET_FW_PROFILE_TYPE2 (icftypes.h)
description: Specifies the type of profile.
helpviewer_keywords: ["NET_FW_PROFILE2_ALL","NET_FW_PROFILE2_DOMAIN","NET_FW_PROFILE2_PRIVATE","NET_FW_PROFILE2_PUBLIC","NET_FW_PROFILE_TYPE2","NET_FW_PROFILE_TYPE2 enumeration [ICS/ICF]","NET_FW_PROFILE_TYPE2_","icftypes/NET_FW_PROFILE2_ALL","icftypes/NET_FW_PROFILE2_DOMAIN","icftypes/NET_FW_PROFILE2_PRIVATE","icftypes/NET_FW_PROFILE2_PUBLIC","icftypes/NET_FW_PROFILE_TYPE2","ics.net_fw_profile_type2"]
old-location: ics\net_fw_profile_type2.htm
tech.root: ics
ms.assetid: cb8328ec-a2eb-4d6f-b6af-214a31a037e9
ms.date: 12/05/2018
ms.keywords: NET_FW_PROFILE2_ALL, NET_FW_PROFILE2_DOMAIN, NET_FW_PROFILE2_PRIVATE, NET_FW_PROFILE2_PUBLIC, NET_FW_PROFILE_TYPE2, NET_FW_PROFILE_TYPE2 enumeration [ICS/ICF], NET_FW_PROFILE_TYPE2_, icftypes/NET_FW_PROFILE2_ALL, icftypes/NET_FW_PROFILE2_DOMAIN, icftypes/NET_FW_PROFILE2_PRIVATE, icftypes/NET_FW_PROFILE2_PUBLIC, icftypes/NET_FW_PROFILE_TYPE2, ics.net_fw_profile_type2
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NET_FW_PROFILE_TYPE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_PROFILE_TYPE2_
 - icftypes/NET_FW_PROFILE_TYPE2_
 - NET_FW_PROFILE_TYPE2
 - icftypes/NET_FW_PROFILE_TYPE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Icftypes.h
api_name:
 - NET_FW_PROFILE_TYPE2
---

# NET_FW_PROFILE_TYPE2 enumeration


## -description

The 
<b>NET_FW_PROFILE_TYPE2</b> enumerated type  specifies the type of profile.

## -enum-fields

### -field NET_FW_PROFILE2_DOMAIN:0x1

Profile type is domain.

### -field NET_FW_PROFILE2_PRIVATE:0x2

Profile type is private. This profile type is used for home and other private network types.

### -field NET_FW_PROFILE2_PUBLIC:0x4

Profile type is public. This profile type is used for public Internet access points.

### -field NET_FW_PROFILE2_ALL:0x7fffffff

## -see-also

<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-enumerated-types">Windows Firewall with Advanced Security Enumerated Types</a>



<a href="/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference">Windows Firewall with Advanced Security Reference</a>
