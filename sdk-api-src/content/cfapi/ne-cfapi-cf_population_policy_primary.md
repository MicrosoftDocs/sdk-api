---
UID: NE:cfapi.CF_POPULATION_POLICY_PRIMARY
title: CF_POPULATION_POLICY_PRIMARY
author: windows-sdk-content
description: Allows a sync provider to control how placeholder directories and files should be created by the platform. This is the primary policy.
old-location: cloudapi\cf_population_policy_primary.htm
tech.root: cfApi
ms.assetid: 3EDCDE3D-AD47-4C4B-9F83-C89879D668DA
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CF_POPULATION_POLICY_ALWAYS_FULL, CF_POPULATION_POLICY_FULL, CF_POPULATION_POLICY_PARTIAL, CF_POPULATION_POLICY_PRIMARY, CF_POPULATION_POLICY_PRIMARY enumeration, PCF_POPULATION_POLICY_PRIMARY, PCF_POPULATION_POLICY_PRIMARY enumeration pointer, cfapi/CF_POPULATION_POLICY_ALWAYS_FULL, cfapi/CF_POPULATION_POLICY_FULL, cfapi/CF_POPULATION_POLICY_PARTIAL, cfapi/CF_POPULATION_POLICY_PRIMARY, cfapi/PCF_POPULATION_POLICY_PRIMARY, cloudApi.cf_population_policy_primary
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
 - CF_POPULATION_POLICY_PRIMARY
product: Windows
targetos: Windows
req.typenames: CF_POPULATION_POLICY_PRIMARY
req.redist: 
---

# CF_POPULATION_POLICY_PRIMARY enumeration


## -description


Allows a sync provider to control how placeholder directories and files should be created by the platform.  This is the primary policy.


## -enum-fields




### -field CF_POPULATION_POLICY_PARTIAL

With <b>CF_POPULATION_POLICY_PARTIAL</b> population policy, when the platform detects access on a not fully populated directory, it will request only the entries required by the user application from the sync provider. This policy is not currently supported by the platform.


### -field CF_POPULATION_POLICY_FULL

With <b>CF_POPULATION_POLICY_FULL</b> population policy, when the platform detects access on a not fully populated directory, it will request the sync provider return all entries under the directory before completing the user request.


### -field CF_POPULATION_POLICY_ALWAYS_FULL

When <b>CF_POPULATION_POLICY_ALWAYS_FULL</b> is selected, the platform assumes that the full name space is always available locally. It will never forward any directory enumeration request to the sync provider.

