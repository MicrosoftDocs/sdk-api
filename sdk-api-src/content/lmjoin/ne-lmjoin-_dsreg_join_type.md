---
UID: NE:lmjoin._DSREG_JOIN_TYPE
title: "_DSREG_JOIN_TYPE"
author: windows-sdk-content
description: Specifies the possible ways that a device can be joined to Microsoft Azure Active Directory.
old-location: netmgmt\dsreg_join_type.htm
old-project: netmgmt
ms.assetid: E29BCBE0-222F-4CA8-97BC-6FE1B6F97A67
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDSREG_JOIN_TYPE, DSREG_DEVICE_JOIN, DSREG_JOIN_TYPE, DSREG_JOIN_TYPE enumeration [Network Management], DSREG_UNKNOWN_JOIN, DSREG_WORKPLACE_JOIN, PDSREG_JOIN_TYPE, PDSREG_JOIN_TYPE enumeration pointer [Network Management], _DSREG_JOIN_TYPE, lmjoin/DSREG_DEVICE_JOIN, lmjoin/DSREG_JOIN_TYPE, lmjoin/DSREG_UNKNOWN_JOIN, lmjoin/DSREG_WORKPLACE_JOIN, lmjoin/PDSREG_JOIN_TYPE, netmgmt.dsreg_join_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DSREG_JOIN_TYPE, *PDSREG_JOIN_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - lmjoin.h
api_name:
 - DSREG_JOIN_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DSREG_JOIN_TYPE enumeration


## -description


Specifies the possible ways that a device can be joined to Microsoft Azure Active Directory.


## -enum-fields




### -field DSREG_UNKNOWN_JOIN

The type of join is not known.


### -field DSREG_DEVICE_JOIN

The device is joined to Azure Active Directory (Azure AD).


### -field DSREG_WORKPLACE_JOIN

An Azure AD work account is added on the device.

