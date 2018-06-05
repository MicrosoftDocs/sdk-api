---
UID: NS:wsman._WSMAN_AUTHZ_QUOTA
title: "_WSMAN_AUTHZ_QUOTA"
author: windows-sdk-content
description: Reports quota information on a per-user basis for authorization plug-ins.
old-location: winrm\wsman_authz_quota.htm
old-project: WinRM
ms.assetid: dff093be-34cb-4e31-b3ff-b1ad8ecc7069
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_AUTHZ_QUOTA, WSMAN_AUTHZ_QUOTA structure [Windows Remote Management], _WSMAN_AUTHZ_QUOTA, winrm.wsman_authz_quota, wsman/WSMAN_AUTHZ_QUOTA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
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
tech.root: 
req.typenames: WSMAN_AUTHZ_QUOTA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsman.h
api_name:
-	WSMAN_AUTHZ_QUOTA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_AUTHZ_QUOTA structure


## -description


Reports quota information on a per-user basis for authorization plug-ins.


## -struct-fields




### -field maxAllowedConcurrentShells

Specifies the maximum number of concurrent shells that a user is allowed to create.


### -field maxAllowedConcurrentOperations

Specifies the maximum number of concurrent operations that a user is allowed to perform. Only top-level operations are counted.  Simple operations such as  get, put, and delete are counted as one operation each. More complex operations are also counted as one. For example,  the enumeration operation and any associated operations that are related to enumeration are counted as one operation.


### -field timeslotSize

Time-slot length for determining the maximum number of operations per time slot.  This value is specified in units of seconds.


### -field maxAllowedOperationsPerTimeslot

Specifies the maximum number of operations allowed per time slot.  This value is used to throttle both top-level and follow-on operations.

