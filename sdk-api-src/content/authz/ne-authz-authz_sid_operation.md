---
UID: NE:authz.AUTHZ_SID_OPERATION
title: AUTHZ_SID_OPERATION
author: windows-sdk-content
description: Indicates the type of SID operations that can be made by a call to the AuthzModifySids function.
old-location: security\authz_sid_operation.htm
old-project: secauthz
ms.assetid: C312BE7D-DA1B-47FE-80BA-7506B9A26E9E
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PAUTHZ_SID_OPERATION, AUTHZ_SID_OPERATION, AUTHZ_SID_OPERATION enumeration [Security], AUTHZ_SID_OPERATION_ADD, AUTHZ_SID_OPERATION_DELETE, AUTHZ_SID_OPERATION_NONE, AUTHZ_SID_OPERATION_REPLACE, AUTHZ_SID_OPERATION_REPLACE_ALL, authz/AUTHZ_SID_OPERATION, authz/AUTHZ_SID_OPERATION_ADD, authz/AUTHZ_SID_OPERATION_DELETE, authz/AUTHZ_SID_OPERATION_NONE, authz/AUTHZ_SID_OPERATION_REPLACE, authz/AUTHZ_SID_OPERATION_REPLACE_ALL, security.authz_sid_operation"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: AUTHZ_SID_OPERATION, *PAUTHZ_SID_OPERATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_SID_OPERATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# AUTHZ_SID_OPERATION enumeration


## -description


The <b>AUTHZ_SID_OPERATION</b> enumeration indicates the type of SID operations that can be made by a call to the <a href="https://msdn.microsoft.com/740569A5-6159-409B-B8CB-B3A8BAE4F398">AuthzModifySids</a> function.


## -enum-fields




### -field AUTHZ_SID_OPERATION_NONE

Do not modify anything.


### -field AUTHZ_SID_OPERATION_REPLACE_ALL

Deletes all existing SIDs and replaces them with the specified SIDs. If the replacement SIDs are not specified, all existing SIDs are deleted. This operation can be specified only once and must be the only operation specified.


### -field AUTHZ_SID_OPERATION_ADD

Adds a new SID. If the SID already exists, the call fails.


### -field AUTHZ_SID_OPERATION_DELETE

Deletes the specified SID. If no matching SID is found, no modifications are done and the call fails.


### -field AUTHZ_SID_OPERATION_REPLACE

Replaces the existing SID with the specified SID. If the SID does not already exist, then adds the SID.

