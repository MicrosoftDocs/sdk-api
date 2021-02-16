---
UID: NS:wtsapi32._WTS_SESSION_ADDRESS
title: WTS_SESSION_ADDRESS (wtsapi32.h)
description: Contains the virtual IP address assigned to a session.
helpviewer_keywords: ["*PWTS_SESSION_ADDRESS","PWTS_SESSION_ADDRESS","PWTS_SESSION_ADDRESS structure pointer [Remote Desktop Services]","WTS_SESSION_ADDRESS","WTS_SESSION_ADDRESS structure [Remote Desktop Services]","termserv.wts_session_address","wtsapi32/PWTS_SESSION_ADDRESS","wtsapi32/WTS_SESSION_ADDRESS"]
old-location: termserv\wts_session_address.htm
tech.root: TermServ
ms.assetid: 4a8846a3-2bad-4ea1-b614-aca18484ea86
ms.date: 12/05/2018
ms.keywords: '*PWTS_SESSION_ADDRESS, PWTS_SESSION_ADDRESS, PWTS_SESSION_ADDRESS structure pointer [Remote Desktop Services], WTS_SESSION_ADDRESS, WTS_SESSION_ADDRESS structure [Remote Desktop Services], termserv.wts_session_address, wtsapi32/PWTS_SESSION_ADDRESS, wtsapi32/WTS_SESSION_ADDRESS'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WTS_SESSION_ADDRESS, *PWTS_SESSION_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_SESSION_ADDRESS
 - wtsapi32/_WTS_SESSION_ADDRESS
 - PWTS_SESSION_ADDRESS
 - wtsapi32/PWTS_SESSION_ADDRESS
 - WTS_SESSION_ADDRESS
 - wtsapi32/WTS_SESSION_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_SESSION_ADDRESS
---

# WTS_SESSION_ADDRESS structure


## -description

Contains the virtual IP address assigned to a session. This structure is returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function when you specify "WTSSessionAddressV4" for the <i>WTSInfoClass</i> parameter.

## -struct-fields

### -field AddressFamily

A null-terminated string that contains the address family. Always set this member to "AF_INET".

### -field Address

The virtual IP address assigned to the session. The format of this address is identical to that used in the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_address">WTS_CLIENT_ADDRESS</a> structure.

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>



<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_address">WTS_CLIENT_ADDRESS</a>