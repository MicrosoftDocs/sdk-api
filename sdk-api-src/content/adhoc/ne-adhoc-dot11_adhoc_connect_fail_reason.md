---
UID: NE:adhoc.tagDOT11_ADHOC_CONNECT_FAIL_REASON
title: DOT11_ADHOC_CONNECT_FAIL_REASON (adhoc.h)
description: Specifies the reason why a connection attempt failed.
helpviewer_keywords: ["DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH","DOT11_ADHOC_CONNECT_FAIL_OTHER","DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH","DOT11_ADHOC_CONNECT_FAIL_REASON","DOT11_ADHOC_CONNECT_FAIL_REASON enumeration [NativeWIFI]","adhoc/DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH","adhoc/DOT11_ADHOC_CONNECT_FAIL_OTHER","adhoc/DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH","adhoc/DOT11_ADHOC_CONNECT_FAIL_REASON","nwifi.dot11_adhoc_connect_fail_reason"]
old-location: nwifi\dot11_adhoc_connect_fail_reason.htm
tech.root: nwifi
ms.assetid: ea95f0b8-14ce-40a6-b5a3-853c414c52af
ms.date: 12/05/2018
ms.keywords: DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH, DOT11_ADHOC_CONNECT_FAIL_OTHER, DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH, DOT11_ADHOC_CONNECT_FAIL_REASON, DOT11_ADHOC_CONNECT_FAIL_REASON enumeration [NativeWIFI], adhoc/DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH, adhoc/DOT11_ADHOC_CONNECT_FAIL_OTHER, adhoc/DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH, adhoc/DOT11_ADHOC_CONNECT_FAIL_REASON, nwifi.dot11_adhoc_connect_fail_reason
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DOT11_ADHOC_CONNECT_FAIL_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDOT11_ADHOC_CONNECT_FAIL_REASON
 - adhoc/tagDOT11_ADHOC_CONNECT_FAIL_REASON
 - DOT11_ADHOC_CONNECT_FAIL_REASON
 - adhoc/DOT11_ADHOC_CONNECT_FAIL_REASON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - adhoc.h
api_name:
 - DOT11_ADHOC_CONNECT_FAIL_REASON
---

# DOT11_ADHOC_CONNECT_FAIL_REASON enumeration


## -description

Specifies the reason why a connection attempt failed.

## -enum-fields

### -field DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH

The local host's configuration is incompatible with the target network. This occurs when the local host is 802.11d compliant and the regulatory domain of the local host is not compatible with the regulatory domain of the target network. For more information about regulatory domains, see the IEEE 802.11d-2001 standard. The standard can be downloaded from the <a href="https://standards.ieee.org/standard">IEEE website</a>.

### -field DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH

The passphrase supplied to authenticate the local machine or user on the target network is incorrect.

### -field DOT11_ADHOC_CONNECT_FAIL_OTHER

The connection failed for another reason.

