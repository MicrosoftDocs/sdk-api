---
UID: NE:cfapi.CF_HARDLINK_POLICY
title: CF_HARDLINK_POLICY
author: windows-sdk-content
description: Specifies whether or not hard links are allowed on placeholder files.
old-location: cloudapi\cf_hardlink_policy.htm
tech.root: cfApi
ms.assetid: 23FFC4E8-0CB7-4FF4-A3C3-2E8FB2C74497
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CF_HARDLINK_POLICY, CF_HARDLINK_POLICY enumeration, CF_HARDLINK_POLICY_ALLOWED, CF_HARDLINK_POLICY_DEFAULT, cfapi/CF_HARDLINK_POLICY, cfapi/CF_HARDLINK_POLICY_ALLOWED, cfapi/CF_HARDLINK_POLICY_DEFAULT, cloudApi.cf_hardlink_policy
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
 - CF_HARDLINK_POLICY
product: Windows
targetos: Windows
req.typenames: CF_HARDLINK_POLICY
req.redist: 
---

# CF_HARDLINK_POLICY enumeration


## -description


Specifies whether or not hard links are allowed on placeholder files.


## -enum-fields




### -field CF_HARDLINK_POLICY_NONE


### -field CF_HARDLINK_POLICY_ALLOWED

Hard links can be created on a placeholder under the same sync root or no sync root. 


#### - CF_HARDLINK_POLICY_DEFAULT

Default; No hard links can be created on any placeholder.


## -remarks



If hard links are enabled, applications can create as many hard links as the file system supports so long as the links are under the same sync root or no sync root. Hard links and placeholder operations that are not compatible with this policy will fail with the error: HRESULT(ERROR_CLOUD_FILES_INCOMPATIBLE_HARDLINKS).



