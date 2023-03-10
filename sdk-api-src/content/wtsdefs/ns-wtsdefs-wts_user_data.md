---
UID: NS:wtsdefs._WTS_USER_DATA
title: WTS_USER_DATA (wtsdefs.h)
description: Contains select client property values.
helpviewer_keywords: ["*PWTS_USER_DATA","PWTS_USER_DATA","PWTS_USER_DATA structure pointer [Remote Desktop Services]","WTS_USER_DATA","WTS_USER_DATA structure [Remote Desktop Services]","termserv.wts_user_data","wtsdefs/PWTS_USER_DATA","wtsdefs/WTS_USER_DATA"]
old-location: termserv\wts_user_data.htm
tech.root: TermServ
ms.assetid: be2f7338-44a8-433f-b45d-620b9b7e93c7
ms.date: 12/05/2018
ms.keywords: '*PWTS_USER_DATA, PWTS_USER_DATA, PWTS_USER_DATA structure pointer [Remote Desktop Services], WTS_USER_DATA, WTS_USER_DATA structure [Remote Desktop Services], termserv.wts_user_data, wtsdefs/PWTS_USER_DATA, wtsdefs/WTS_USER_DATA'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: WTS_USER_DATA, *PWTS_USER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTS_USER_DATA
 - wtsdefs/_WTS_USER_DATA
 - PWTS_USER_DATA
 - wtsdefs/PWTS_USER_DATA
 - WTS_USER_DATA
 - wtsdefs/WTS_USER_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_USER_DATA
---

# WTS_USER_DATA structure


## -description

Contains select client property values.

## -struct-fields

### -field WorkDirectory

A string value that specifies the directory where the client startup program resides. This value corresponds to the <b>WorkDirectory</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_client_data">WTS_CLIENT_DATA</a> structure.

### -field InitialProgram

A string value that specifies the name of  the initial program. This value corresponds to the <b>InitialProgram</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_client_data">WTS_CLIENT_DATA</a> structure.

### -field UserTimeZone

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_time_zone_information">WTS_TIME_ZONE_INFORMATION</a> structure that contains client time zone information. This value corresponds to the <b>ClientTimeZone</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_client_data">WTS_CLIENT_DATA</a> structure.

## -remarks

This structure is used by the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata">GetUserData</a> method and is both sent to and returned by the protocol. This structure is initialized with client data by the Remote Desktop Services service. If a value does not exist for a member, the protocol should not provide one.