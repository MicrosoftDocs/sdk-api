---
UID: NE:cfapi.CF_REGISTER_FLAGS
title: CF_REGISTER_FLAGS (cfapi.h)
author: windows-sdk-content
description: Flags for registering and updating a sync root.
old-location: cloudapi\cf_register_flags.htm
tech.root: cfApi
ms.assetid: 043670D7-5908-40B5-82A8-EFF05FCB391B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CF_REGISTER_FLAGS, CF_REGISTER_FLAGS enumeration, CF_REGISTER_FLAG_DISABLE_ON_DEMAND_POPULATION_ON_ROOT, CF_REGISTER_FLAG_MARK_IN_SYNC_ON_ROOT, CF_REGISTER_FLAG_NONE, CF_REGISTER_FLAG_UPDATE, cfapi/CF_REGISTER_FLAGS, cfapi/CF_REGISTER_FLAG_DISABLE_ON_DEMAND_POPULATION_ON_ROOT, cfapi/CF_REGISTER_FLAG_MARK_IN_SYNC_ON_ROOT, cfapi/CF_REGISTER_FLAG_NONE, cfapi/CF_REGISTER_FLAG_UPDATE, cloudApi.cf_register_flags
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
 - CF_REGISTER_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_REGISTER_FLAGS
req.redist: 
ms.custom: 19H1
---

# CF_REGISTER_FLAGS enumeration


## -description


Flags for registering and updating a sync root.


## -enum-fields




### -field CF_REGISTER_FLAG_NONE

No registration flags.


### -field CF_REGISTER_FLAG_UPDATE

Use this flag for modifying previously registered sync root identities and policies.


### -field CF_REGISTER_FLAG_DISABLE_ON_DEMAND_POPULATION_ON_ROOT

The on-demand directory/folder population behavior is globally controlled by the population policy. This flag allows a sync provider to opt out of the on-demand population behavior just for the sync root itself while keeping on-demand population on for all other directories under the sync root. This is useful when the sync provider would like to pre-populate the immediate child files/directories of the sync root.


### -field CF_REGISTER_FLAG_MARK_IN_SYNC_ON_ROOT

This flag allows a sync provider to mark the sync root to be registered in-sync simultaneously at the registration time. An alternative is to call <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/nf-cfapi-cfsetinsyncstate">CfSetInSyncState</a> on the sync root later. 

