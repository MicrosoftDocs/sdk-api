---
UID: NS:lmjoin._DSREG_USER_INFO
title: "_DSREG_USER_INFO"
author: windows-sdk-content
description: Contains information about a user account that is used to join a device to Microsoft Azure Active Directory.
old-location: netmgmt\dsreg_user_info.htm
old-project: netmgmt
ms.assetid: 5E639988-0F53-40D7-BBEC-F78B3D124CC0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDSREG_USER_INFO, DSREG_USER_INFO, DSREG_USER_INFO structure [Network Management], PDSREG_USER_INFO, PDSREG_USER_INFO structure pointer [Network Management], _DSREG_USER_INFO, lmjoin/DSREG_USER_INFO, lmjoin/PDSREG_USER_INFO, netmgmt.dsreg_user_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmjoin.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DSREG_USER_INFO, *PDSREG_USER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - lmjoin.h
api_name:
 - DSREG_USER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DSREG_USER_INFO structure


## -description


Contains information about a user account  that is used to join a device to Microsoft Azure Active Directory.


## -struct-fields




### -field pszUserEmail

The email address of the user.


### -field pszUserKeyId

The identifier of the Microsoft Passport key that is provisioned for the user.


### -field pszUserKeyName

The name of the Microsoft Passport key that is provisioned for the user.

