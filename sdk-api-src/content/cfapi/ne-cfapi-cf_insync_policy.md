---
UID: NE:cfapi.CF_INSYNC_POLICY
title: CF_INSYNC_POLICY (cfapi.h)
author: windows-sdk-content
description: A policy allowing a sync provider to control when the platform should clear the in-sync state on a placeholder file or directory.
old-location: cloudapi\cf_insync_policy.htm
tech.root: cfApi
ms.assetid: BE9574D7-2717-42F6-AB59-096AACCD8BC1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CF_INSYNC_POLICY, CF_INSYNC_POLICY enumeration, CF_INSYNC_POLICY_DEFAULT, CF_INSYNC_POLICY_PRESERVE_INSYNC_FOR_SYNC_ENGINE, CF_INSYNC_POLICY_TRACK_ALL, CF_INSYNC_POLICY_TRACK_DIRECTORY_ALL, CF_INSYNC_POLICY_TRACK_DIRECTORY_CREATION_TIME, CF_INSYNC_POLICY_TRACK_DIRECTORY_HIDDEN_ATTRIBUTE, CF_INSYNC_POLICY_TRACK_DIRECTORY_LAST_WRITE_TIME, CF_INSYNC_POLICY_TRACK_DIRECTORY_READONLY_ATTRIBUTE, CF_INSYNC_POLICY_TRACK_DIRECTORY_SYSTEM_ATTRIBUTE, CF_INSYNC_POLICY_TRACK_FILE_ALL, CF_INSYNC_POLICY_TRACK_FILE_CREATION_TIME, CF_INSYNC_POLICY_TRACK_FILE_HIDDEN_ATTRIBUTE, CF_INSYNC_POLICY_TRACK_FILE_LAST_WRITE_TIME, CF_INSYNC_POLICY_TRACK_FILE_READONLY_ATTRIBUTE, CF_INSYNC_POLICY_TRACK_SYSTEM_ATTRIBUTE, cfapi/CF_INSYNC_POLICY, cfapi/CF_INSYNC_POLICY_DEFAULT, cfapi/CF_INSYNC_POLICY_PRESERVE_INSYNC_FOR_SYNC_ENGINE, cfapi/CF_INSYNC_POLICY_TRACK_ALL, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_ALL, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_CREATION_TIME, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_HIDDEN_ATTRIBUTE, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_LAST_WRITE_TIME, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_READONLY_ATTRIBUTE, cfapi/CF_INSYNC_POLICY_TRACK_DIRECTORY_SYSTEM_ATTRIBUTE, cfapi/CF_INSYNC_POLICY_TRACK_FILE_ALL, cfapi/CF_INSYNC_POLICY_TRACK_FILE_CREATION_TIME, cfapi/CF_INSYNC_POLICY_TRACK_FILE_HIDDEN_ATTRIBUTE, cfapi/CF_INSYNC_POLICY_TRACK_FILE_LAST_WRITE_TIME, cfapi/CF_INSYNC_POLICY_TRACK_FILE_READONLY_ATTRIBUTE, cfapi/CF_INSYNC_POLICY_TRACK_SYSTEM_ATTRIBUTE, cloudApi.cf_insync_policy
ms.topic: enum
f1_keywords: 
 - "cfapi/CF_INSYNC_POLICY"
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
 - CF_INSYNC_POLICY
targetos: Windows
req.typenames: CF_INSYNC_POLICY
req.redist: 
ms.custom: 19H1
---

# CF_INSYNC_POLICY enumeration


## -description


A policy allowing a sync provider to control when the platform should clear the in-sync state on a placeholder file or directory.


## -enum-fields




### -field CF_INSYNC_POLICY_NONE


### -field CF_INSYNC_POLICY_TRACK_FILE_CREATION_TIME

Clears in-sync state when a file is created.


### -field CF_INSYNC_POLICY_TRACK_FILE_READONLY_ATTRIBUTE

Clears in-sync state when a file is read-only.


### -field CF_INSYNC_POLICY_TRACK_FILE_HIDDEN_ATTRIBUTE

Clears in-sync state when a file is hidden.


### -field CF_INSYNC_POLICY_TRACK_FILE_SYSTEM_ATTRIBUTE


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_CREATION_TIME

Clears in-sync state when a directory is created.


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_READONLY_ATTRIBUTE

Clears in-sync state when a directory is read-only.


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_HIDDEN_ATTRIBUTE

Clears in-sync state when a directory is hidden.


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_SYSTEM_ATTRIBUTE

Clears in-sync state when a directory is  a system directory.


### -field CF_INSYNC_POLICY_TRACK_FILE_LAST_WRITE_TIME

Clears in-sync state based on the last write time to a file.


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_LAST_WRITE_TIME

Clears in-sync state based on the last write time to a directory.


### -field CF_INSYNC_POLICY_TRACK_FILE_ALL

Clears in-sync state for any changes to a file.


### -field CF_INSYNC_POLICY_TRACK_DIRECTORY_ALL

Clears in-sync state for any changes to a directory.


### -field CF_INSYNC_POLICY_TRACK_ALL

Clears in-sync state for any changes to a file or directory.


### -field CF_INSYNC_POLICY_PRESERVE_INSYNC_FOR_SYNC_ENGINE

In-sync policies are exempt from clearing.


#### - CF_INSYNC_POLICY_DEFAULT

The default in-sync policy.


#### - CF_INSYNC_POLICY_TRACK_SYSTEM_ATTRIBUTE

Clears in-sync state when a file is a system file.

