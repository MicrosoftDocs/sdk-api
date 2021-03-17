---
UID: NS:lmjoin._DSREG_USER_INFO
title: DSREG_USER_INFO (lmjoin.h)
description: Contains information about a user account that is used to join a device to Microsoft Azure Active Directory.
helpviewer_keywords: ["*PDSREG_USER_INFO","DSREG_USER_INFO","DSREG_USER_INFO structure [Network Management]","PDSREG_USER_INFO","PDSREG_USER_INFO structure pointer [Network Management]","lmjoin/DSREG_USER_INFO","lmjoin/PDSREG_USER_INFO","netmgmt.dsreg_user_info"]
old-location: netmgmt\dsreg_user_info.htm
tech.root: NetMgmt
ms.assetid: 5E639988-0F53-40D7-BBEC-F78B3D124CC0
ms.date: 12/05/2018
ms.keywords: '*PDSREG_USER_INFO, DSREG_USER_INFO, DSREG_USER_INFO structure [Network Management], PDSREG_USER_INFO, PDSREG_USER_INFO structure pointer [Network Management], lmjoin/DSREG_USER_INFO, lmjoin/PDSREG_USER_INFO, netmgmt.dsreg_user_info'
req.header: lmjoin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: DSREG_USER_INFO, *PDSREG_USER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSREG_USER_INFO
 - lmjoin/_DSREG_USER_INFO
 - PDSREG_USER_INFO
 - lmjoin/PDSREG_USER_INFO
 - DSREG_USER_INFO
 - lmjoin/DSREG_USER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - lmjoin.h
api_name:
 - DSREG_USER_INFO
---

# DSREG_USER_INFO structure


## -description

Contains information about a user account  that is used to join a device to Microsoft Azure Active Directory.

## -struct-fields

### -field pszUserEmail

The email address of the user.

### -field pszUserKeyId

The identifier of the Microsoft Passport key that is provisioned for the user.

### -field pszUserKeyName

The name of the Microsoft Passport key that is provisioned for the user.

