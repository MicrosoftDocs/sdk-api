---
UID: NE:cfapi.CF_CREATE_FLAGS
title: CF_CREATE_FLAGS
author: windows-driver-content
description: Flags for creating a placeholder file or directory.
old-location: cloudapi\cf_create_flags.htm
old-project: cfApi
ms.assetid: F70ECFDB-8542-4395-9EDD-7DABC2E5225D
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PCF_CREATE_FLAGS, CF_CREATE_FLAGS, CF_CREATE_FLAGS enumeration, CF_CREATE_FLAG_NONE, CF_CREATE_FLAG_STOP_ON_ERROR, PCF_CREATE_FLAGS, PCF_CREATE_FLAGS enumeration pointer, cfapi/CF_CREATE_FLAGS, cfapi/CF_CREATE_FLAG_NONE, cfapi/CF_CREATE_FLAG_STOP_ON_ERROR, cfapi/PCF_CREATE_FLAGS, cloudApi.cf_create_flags"
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
req.typenames: CF_CREATE_FLAGS, *PCF_CREATE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CfApi.h
api_name:
-	CF_CREATE_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CREATE_FLAGS enumeration


## -description


Flags for creating a placeholder file or directory.


## -enum-fields




### -field CF_CREATE_FLAG_NONE

Default mode. All entries are processed.


### -field CF_CREATE_FLAG_STOP_ON_ERROR

Causes the API to return immediately if placeholder creation fails. If creation fails, the error code will be returned by the API.

