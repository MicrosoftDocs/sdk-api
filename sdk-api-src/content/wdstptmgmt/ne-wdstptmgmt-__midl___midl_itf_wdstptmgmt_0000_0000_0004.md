---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0004
title: "__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0004"
author: windows-sdk-content
description: Indicates what action a WDS client should take when it is disconnected from the session.
old-location: wds\wdstransport_disconnect_type.htm
tech.root: wds
ms.assetid: f25bdc9e-0014-4ff7-bc01-8a13b6e3ace1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PWDSTRANSPORT_DISCONNECT_TYPE, WDSTRANSPORT_DISCONNECT_TYPE, WDSTRANSPORT_DISCONNECT_TYPE enumeration [Windows Deployment Services], WdsTptDisconnectAbort, WdsTptDisconnectFallback, WdsTptDisconnectUnknown, __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0004, wds.wdstransport_disconnect_type, wdstptmgmt/WDSTRANSPORT_DISCONNECT_TYPE, wdstptmgmt/WdsTptDisconnectAbort, wdstptmgmt/WdsTptDisconnectFallback, wdstptmgmt/WdsTptDisconnectUnknown"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_DISCONNECT_TYPE
product: Windows
targetos: Windows
req.typenames: WDSTRANSPORT_DISCONNECT_TYPE, *PWDSTRANSPORT_DISCONNECT_TYPE
req.redist: 
---

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0004 enumeration


## -description


Indicates what action a WDS client should take when it is disconnected from the session.


## -enum-fields




### -field WdsTptDisconnectUnknown

Default value that indicates that the disconnection type is not known.


### -field WdsTptDisconnectFallback

Indicates that the client should leave the session and fallback to an alternate mechanism for retrieving data. For example, a client disconnected from a multicast session can try using unicast instead.


### -field WdsTptDisconnectAbort

Indicates that the client should leave the session and abort all attempts to retrieve the data from this server.

