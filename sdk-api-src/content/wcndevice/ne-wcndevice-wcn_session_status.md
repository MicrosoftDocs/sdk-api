---
UID: NE:wcndevice.tagWCN_SESSION_STATUS
title: WCN_SESSION_STATUS (wcndevice.h)
description: Defines the outcome status of a WPS session.helpviewer_keywords: ["WCN_SESSION_FAILURE_GENERIC","WCN_SESSION_FAILURE_TIMEOUT","WCN_SESSION_STATUS","WCN_SESSION_STATUS enumeration [Windows Connect Now]","WCN_SESSION_STATUS_SUCCESS","wcn.wcn_session_status","wcndevice/WCN_SESSION_FAILURE_GENERIC","wcndevice/WCN_SESSION_FAILURE_TIMEOUT","wcndevice/WCN_SESSION_STATUS","wcndevice/WCN_SESSION_STATUS_SUCCESS"]
old-location: wcn\wcn_session_status.htm
tech.root: wcn
ms.assetid: 131D24B7-3D0D-4683-A7EA-94F5DC1E504C
ms.date: 12/05/2018
ms.keywords: WCN_SESSION_FAILURE_GENERIC, WCN_SESSION_FAILURE_TIMEOUT, WCN_SESSION_STATUS, WCN_SESSION_STATUS enumeration [Windows Connect Now], WCN_SESSION_STATUS_SUCCESS, wcn.wcn_session_status, wcndevice/WCN_SESSION_FAILURE_GENERIC, wcndevice/WCN_SESSION_FAILURE_TIMEOUT, wcndevice/WCN_SESSION_STATUS, wcndevice/WCN_SESSION_STATUS_SUCCESS
f1_keywords:
- wcndevice/WCN_SESSION_STATUS
dev_langs:
- c++
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- wcndevice.h
api_name:
- WCN_SESSION_STATUS
targetos: Windows
req.typenames: WCN_SESSION_STATUS
req.redist: 
ms.custom: 19H1
---

# WCN_SESSION_STATUS enumeration


## -description


The <b>WCN_SESSION_STATUS</b>  enumeration defines the outcome status of a WPS session.


## -enum-fields




### -field WCN_SESSION_STATUS_SUCCESS

Indicates that the session is successful.


### -field WCN_SESSION_STATUS_FAILURE_GENERIC


### -field WCN_SESSION_STATUS_FAILURE_TIMEOUT




#### - WCN_SESSION_FAILURE_GENERIC

Indicates that the session has failed.


#### - WCN_SESSION_FAILURE_TIMEOUT

Indicates that the session has failed due to a timeout.

