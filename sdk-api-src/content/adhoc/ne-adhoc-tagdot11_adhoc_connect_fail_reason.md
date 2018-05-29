---
UID: NE:adhoc.tagDOT11_ADHOC_CONNECT_FAIL_REASON
title: tagDOT11_ADHOC_CONNECT_FAIL_REASON
author: windows-sdk-content
description: Specifies the reason why a connection attempt failed.
old-location: nwifi\dot11_adhoc_connect_fail_reason.htm
old-project: NativeWiFi
ms.assetid: ea95f0b8-14ce-40a6-b5a3-853c414c52af
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH, DOT11_ADHOC_CONNECT_FAIL_OTHER, DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH, DOT11_ADHOC_CONNECT_FAIL_REASON, DOT11_ADHOC_CONNECT_FAIL_REASON enumeration [NativeWIFI], adhoc/DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH, adhoc/DOT11_ADHOC_CONNECT_FAIL_OTHER, adhoc/DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH, adhoc/DOT11_ADHOC_CONNECT_FAIL_REASON, nwifi.dot11_adhoc_connect_fail_reason, tagDOT11_ADHOC_CONNECT_FAIL_REASON
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: DOT11_ADHOC_CONNECT_FAIL_REASON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	adhoc.h
api_name:
-	DOT11_ADHOC_CONNECT_FAIL_REASON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagDOT11_ADHOC_CONNECT_FAIL_REASON enumeration


## -description


Specifies the reason why a connection attempt failed. 


## -enum-fields




### -field DOT11_ADHOC_CONNECT_FAIL_DOMAIN_MISMATCH

The local host's configuration is incompatible with the target network. This occurs when the local host is 802.11d compliant and the regulatory domain of the local host is not compatible with the regulatory domain of the target network. For more information about regulatory domains, see the IEEE 802.11d-2001 standard. The standard can be downloaded from the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83977">IEEE website</a>.


### -field DOT11_ADHOC_CONNECT_FAIL_PASSPHRASE_MISMATCH

The passphrase supplied to authenticate the local machine or user on the target network is incorrect.


### -field DOT11_ADHOC_CONNECT_FAIL_OTHER

The connection failed for another reason.

