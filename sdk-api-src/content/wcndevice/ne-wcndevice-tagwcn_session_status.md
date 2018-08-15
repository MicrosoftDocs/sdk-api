---
UID: NE:wcndevice.tagWCN_SESSION_STATUS
title: tagWCN_SESSION_STATUS
author: windows-sdk-content
description: Defines the outcome status of a WPS session.
old-location: wcn\wcn_session_status.htm
old-project: wcn
ms.assetid: 131D24B7-3D0D-4683-A7EA-94F5DC1E504C
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WCN_SESSION_FAILURE_GENERIC, WCN_SESSION_FAILURE_TIMEOUT, WCN_SESSION_STATUS, WCN_SESSION_STATUS enumeration [Windows Connect Now], WCN_SESSION_STATUS_SUCCESS, tagWCN_SESSION_STATUS, wcn.wcn_session_status, wcndevice/WCN_SESSION_FAILURE_GENERIC, wcndevice/WCN_SESSION_FAILURE_TIMEOUT, wcndevice/WCN_SESSION_STATUS, wcndevice/WCN_SESSION_STATUS_SUCCESS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wcndevice.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_SESSION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wcndevice.h
api_name:
 - WCN_SESSION_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# tagWCN_SESSION_STATUS enumeration


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

