---
UID: NE:icftypes.NET_FW_AUTHENTICATE_TYPE_
title: NET_FW_AUTHENTICATE_TYPE (icftypes.h)
description: Specifies the type of authentication which must occur in order for traffic to be allowed.
helpviewer_keywords: ["NET_FW_AUTHENTICATE_AND_ENCRYPT","NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION","NET_FW_AUTHENTICATE_NONE","NET_FW_AUTHENTICATE_NO_ENCAPSULATION","NET_FW_AUTHENTICATE_TYPE","NET_FW_AUTHENTICATE_TYPE enumeration [ICS/ICF]","NET_FW_AUTHENTICATE_WITH_INTEGRITY","icftypes/NET_FW_AUTHENTICATE_AND_ENCRYPT","icftypes/NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION","icftypes/NET_FW_AUTHENTICATE_NONE","icftypes/NET_FW_AUTHENTICATE_NO_ENCAPSULATION","icftypes/NET_FW_AUTHENTICATE_TYPE","icftypes/NET_FW_AUTHENTICATE_WITH_INTEGRITY","ics.net_fw_authenticate_type"]
old-location: ics\net_fw_authenticate_type.htm
tech.root: ics
ms.assetid: 65ace93f-0e27-4cfd-befe-9b94e05e3244
ms.date: 12/05/2018
ms.keywords: NET_FW_AUTHENTICATE_AND_ENCRYPT, NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION, NET_FW_AUTHENTICATE_NONE, NET_FW_AUTHENTICATE_NO_ENCAPSULATION, NET_FW_AUTHENTICATE_TYPE, NET_FW_AUTHENTICATE_TYPE enumeration [ICS/ICF], NET_FW_AUTHENTICATE_WITH_INTEGRITY, icftypes/NET_FW_AUTHENTICATE_AND_ENCRYPT, icftypes/NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION, icftypes/NET_FW_AUTHENTICATE_NONE, icftypes/NET_FW_AUTHENTICATE_NO_ENCAPSULATION, icftypes/NET_FW_AUTHENTICATE_TYPE, icftypes/NET_FW_AUTHENTICATE_WITH_INTEGRITY, ics.net_fw_authenticate_type
req.header: icftypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: NET_FW_AUTHENTICATE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NET_FW_AUTHENTICATE_TYPE_
 - icftypes/NET_FW_AUTHENTICATE_TYPE_
 - NET_FW_AUTHENTICATE_TYPE
 - icftypes/NET_FW_AUTHENTICATE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - icftypes.h
api_name:
 - NET_FW_AUTHENTICATE_TYPE
---

# NET_FW_AUTHENTICATE_TYPE enumeration


## -description

The <b>NET_FW_AUTHENTICATE_TYPE</b> enumerated type specifies the type of authentication which must occur in order for traffic to be allowed..

## -enum-fields

### -field NET_FW_AUTHENTICATE_NONE:0

No security check is performed.

### -field NET_FW_AUTHENTICATE_NO_ENCAPSULATION

The traffic is allowed if it is IPsec-protected with authentication and no encapsulation protection. This means that the peer is authenticated, but there is no integrity protection on the data.

### -field NET_FW_AUTHENTICATE_WITH_INTEGRITY

The traffic is allowed if it is IPsec-protected with authentication and integrity protection.

### -field NET_FW_AUTHENTICATE_AND_NEGOTIATE_ENCRYPTION

The traffic is allowed if its is IPsec-protected with authentication and integrity protection. In addition, negotiation of encryption protections on subsequent packets is requested.

### -field NET_FW_AUTHENTICATE_AND_ENCRYPT

The traffic is allowed if it is IPsec-protected with authentication, integrity and encryption protection since the very first packet.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule3-get_secureflags">INetFwRule3::SecureFlags </a>
