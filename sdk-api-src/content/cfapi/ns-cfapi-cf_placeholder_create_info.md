---
UID: NS:cfapi.CF_PLACEHOLDER_CREATE_INFO
title: CF_PLACEHOLDER_CREATE_INFO
author: windows-sdk-content
description: Contains placeholder information for creating new placeholder files or directories.
old-location: cloudapi\cf_placeholder_create_info.htm
old-project: cfApi
ms.assetid: 2DC1FF5F-FBFD-45CA-8CD5-B2F586C22778
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_PLACEHOLDER_CREATE_INFO, CF_PLACEHOLDER_CREATE_INFO structure, cfapi/CF_PLACEHOLDER_CREATE_INFO, cloudApi.cf_placeholder_create_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CF_PLACEHOLDER_CREATE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PLACEHOLDER_CREATE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_PLACEHOLDER_CREATE_INFO structure


## -description


Contains placeholder information for creating new placeholder files or directories. 


## -struct-fields




### -field RelativeFileName

The name of the child placeholder file or directory to be created.


### -field FsMetadata

File system metadata to be created with the placeholder. 


### -field FileIdentity

A user mode buffer containing file information supplied by the sync provider. This is required for files (not for directories).


### -field FileIdentityLength

Length, in bytes, of the <b>FileIdentity</b>.


### -field Flags

Flags for specifying placeholder creation behavior.


### -field Result

The result of placeholder creation. On successful creation, the value is: STATUS_OK.


### -field CreateUsn

The final USN value after create actions are performed.

