---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0010
title: WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE (wdstptmgmt.h)
description: Specifies the type of automatic actions a WDS transport server, running on Windows Server 2008 R2, should use to handle a client computer that is slowing the multicast transmission.
helpviewer_keywords: ["*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE enumeration [Windows Deployment Services]","WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE enumeration [Windows Deployment Services]","WdsTptSlowClientHandlingAutoDisconnect","WdsTptSlowClientHandlingMultistream","WdsTptSlowClientHandlingNone","WdsTptSlowClientHandlingUnknown","wds.wdstransport_slow_client_handling_type","wdstptmgmt/WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE","wdstptmgmt/WdsTptSlowClientHandlingAutoDisconnect","wdstptmgmt/WdsTptSlowClientHandlingMultistream","wdstptmgmt/WdsTptSlowClientHandlingNone","wdstptmgmt/WdsTptSlowClientHandlingUnknown"]
old-location: wds\wdstransport_slow_client_handling_type.htm
tech.root: wds
ms.assetid: e15e67c3-ad39-4504-bd38-1b291082d196
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE, WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE, WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE enumeration [Windows Deployment Services], WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE,*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE, WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE,*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE enumeration [Windows Deployment Services], WdsTptSlowClientHandlingAutoDisconnect, WdsTptSlowClientHandlingMultistream, WdsTptSlowClientHandlingNone, WdsTptSlowClientHandlingUnknown, wds.wdstransport_slow_client_handling_type, wdstptmgmt/WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE, wdstptmgmt/WdsTptSlowClientHandlingAutoDisconnect, wdstptmgmt/WdsTptSlowClientHandlingMultistream, wdstptmgmt/WdsTptSlowClientHandlingNone, wdstptmgmt/WdsTptSlowClientHandlingUnknown'
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE, *PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0010
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0010
 - PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
 - wdstptmgmt/PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
 - WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
 - wdstptmgmt/WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE,*PWDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE
---

# WDSTRANSPORT_SLOW_CLIENT_HANDLING_TYPE enumeration


## -description

Specifies the type of automatic actions a WDS transport server, running on Windows Server 2008 R2, should use to handle a client computer that is slowing the multicast transmission.

## -enum-fields

### -field WdsTptSlowClientHandlingUnknown:0

Default value that indicates the automatic action used to handle slow client computers is not known.

### -field WdsTptSlowClientHandlingNone:1

Indicates that the server takes no action on any clients that are slowing the multicast transmission.

### -field WdsTptSlowClientHandlingAutoDisconnect:2

Indicates that the server detects clients that are slowing the multicast transmission below a configured threshold. Depending on a configurable setting, the server disconnects the slow clients from the multicast transmission or instructs the slow clients to fallback to an alternate mechanism for retrieving data. For example, a client disconnected from a multicast session can try using unicast instead.

### -field WdsTptSlowClientHandlingMultistream:3

Indicates that the server detects clients that are slowing the multicast transmission below a specified percentage of available bandwidth. The server moves the slow clients to lower-speed streams of the same multicast transmission. The server cannot move legacy clients that do not support the multistream handling option, and in this case, the server disconnects the client or instructs the client to fallback depending upon the <a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportmulticastsessionpolicy-get_slowclientfallback">SlowClientFallback</a> property.
