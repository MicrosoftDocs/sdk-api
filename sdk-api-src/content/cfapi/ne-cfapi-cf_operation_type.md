---
UID: NE:cfapi.CF_OPERATION_TYPE
title: CF_OPERATION_TYPE
author: windows-sdk-content
description: The types of operations that can be performed on placeholder files and directories.
old-location: cloudapi\cf_operation_type.htm
tech.root: cfApi
ms.assetid: 34E23442-1BCC-4B8B-9AD3-67B2AEDBE2FE
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CF_OPERATION_TYPE, CF_OPERATION_TYPE enumeration, CF_OPERATION_TYPE_ACK_DATA, CF_OPERATION_TYPE_ACK_DEHYDRATE, CF_OPERATION_TYPE_ACK_DELETE, CF_OPERATION_TYPE_ACK_RENAME, CF_OPERATION_TYPE_RESTART_HYDRATION, CF_OPERATION_TYPE_RETRIEVE_DATA, CF_OPERATION_TYPE_TRANSFER_DATA, CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS, cfapi/CF_OPERATION_TYPE, cfapi/CF_OPERATION_TYPE_ACK_DATA, cfapi/CF_OPERATION_TYPE_ACK_DEHYDRATE, cfapi/CF_OPERATION_TYPE_ACK_DELETE, cfapi/CF_OPERATION_TYPE_ACK_RENAME, cfapi/CF_OPERATION_TYPE_RESTART_HYDRATION, cfapi/CF_OPERATION_TYPE_RETRIEVE_DATA, cfapi/CF_OPERATION_TYPE_TRANSFER_DATA, cfapi/CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS, cloudApi.cf_operation_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_OPERATION_TYPE
product: Windows
targetos: Windows
req.typenames: CF_OPERATION_TYPE
req.redist: 
---

# CF_OPERATION_TYPE enumeration


## -description


The types of operations that can be performed on placeholder files and directories.


## -enum-fields




### -field CF_OPERATION_TYPE_TRANSFER_DATA

Transfers data to hydrate a placeholder.


### -field CF_OPERATION_TYPE_RETRIEVE_DATA

Validates the integrity of data previously transferred to a placeholder.


### -field CF_OPERATION_TYPE_ACK_DATA

Data is acknowledged by the sync provider. 


### -field CF_OPERATION_TYPE_RESTART_HYDRATION

Restarts ongoing data hydration.


### -field CF_OPERATION_TYPE_TRANSFER_PLACEHOLDERS

Transfers placeholders.


### -field CF_OPERATION_TYPE_ACK_DEHYDRATE

Acknowledge and dehydrate a placeholder.


### -field CF_OPERATION_TYPE_ACK_DELETE

Acknowledge and delete a placeholder.


### -field CF_OPERATION_TYPE_ACK_RENAME

Acknowledge and rename a placeholder.

