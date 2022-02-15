---
UID: NE:icftypes.NET_FW_PROFILE_TYPE_
title: NET_FW_PROFILE_TYPE (icftypes.h)
description: Specifies the type of profile.
helpviewer_keywords: ["NET_FW_PROFILE_CURRENT","NET_FW_PROFILE_DOMAIN","NET_FW_PROFILE_STANDARD","NET_FW_PROFILE_TYPE","NET_FW_PROFILE_TYPE enumeration [ICS/ICF]","NET_FW_PROFILE_TYPE_","NET_FW_PROFILE_TYPE_MAX","icftypes/NET_FW_PROFILE_CURRENT","icftypes/NET_FW_PROFILE_DOMAIN","icftypes/NET_FW_PROFILE_STANDARD","icftypes/NET_FW_PROFILE_TYPE","icftypes/NET_FW_PROFILE_TYPE_MAX","ics.net_fw_profile_type"]
old-location: ics\net_fw_profile_type.htm
tech.root: ics
ms.assetid: abf59405-86c7-4a20-a3e9-b12b27290b00
ms.date: 12/05/2018
ms.keywords: NET_FW_PROFILE_CURRENT, NET_FW_PROFILE_DOMAIN, NET_FW_PROFILE_STANDARD, NET_FW_PROFILE_TYPE, NET_FW_PROFILE_TYPE enumeration [ICS/ICF], NET_FW_PROFILE_TYPE_, NET_FW_PROFILE_TYPE_MAX, icftypes/NET_FW_PROFILE_CURRENT, icftypes/NET_FW_PROFILE_DOMAIN, icftypes/NET_FW_PROFILE_STANDARD, icftypes/NET_FW_PROFILE_TYPE, icftypes/NET_FW_PROFILE_TYPE_MAX, ics.net_fw_profile_type
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: NET_FW_PROFILE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_PROFILE_TYPE_
 - icftypes/NET_FW_PROFILE_TYPE_
 - NET_FW_PROFILE_TYPE
 - icftypes/NET_FW_PROFILE_TYPE
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
 - NET_FW_PROFILE_TYPE
---

# NET_FW_PROFILE_TYPE enumeration


## -description

> [!NOTE]
>The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the [Firewall with Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)Windows API is recommended.

The **NET_FW_PROFILE_TYPE** enumerated type  specifies the type of profile.

## -enum-fields

### -field NET_FW_PROFILE_DOMAIN:0

Profile type is domain.

### -field NET_FW_PROFILE_STANDARD

Profile type is standard.

### -field NET_FW_PROFILE_CURRENT

Profile type is current.

### -field NET_FW_PROFILE_TYPE_MAX

Used for boundary checking only. Not valid for application programming.

## -see-also

[Windows Firewall Enumerated Types](/previous-versions/windows/desktop/ics/windows-firewall-enumerated-types)

[Windows Firewall Reference](/previous-versions/windows/desktop/ics/windows-firewall-reference)
