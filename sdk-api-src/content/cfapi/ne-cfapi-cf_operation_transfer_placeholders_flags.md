---
UID: NE:cfapi.CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
title: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
author: windows-sdk-content
description: Flags to specify the behavior when transferring a placeholder file or directory.
old-location: cloudapi\cf_operation_transfer_placeholders_flags.htm
tech.root: cfApi
ms.assetid: 6C75030D-A5CF-423D-A931-3D2ED6113BD1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE, CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE, cfapi/CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR, cloudApi.cf_operation_transfer_placeholders_flags
ms.prod: windows
ms.technology: windows-sdk
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
 - CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS
req.redist: 
---

# CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAGS enumeration


## -description


Flags to specify the behavior when transferring a placeholder file or directory.


## -enum-fields




### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_NONE

No transfer placeholder flags.


### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_STOP_ON_ERROR

Causes the API to return immediately if a placeholder transfer fails. If a transfer fails, the error code will be returned.


### -field CF_OPERATION_TRANSFER_PLACEHOLDERS_FLAG_DISABLE_ON_DEMAND_POPULATION

The transferred child placeholder directory is considered to have all of its children present locally.

Applicable to a child placeholder directory only.

