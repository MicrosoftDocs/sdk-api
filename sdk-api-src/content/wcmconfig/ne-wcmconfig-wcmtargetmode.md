---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0001
title: WcmTargetMode (wcmconfig.h)
author: windows-sdk-content
description: Enumerates the various target modes.
old-location: smi\wcmtargetmode.htm
tech.root: SMI
ms.assetid: 7a3b61f4-c98f-4c59-98dd-b513f69ac7d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OfflineMode, OnlineMode, WcmTargetMode, WcmTargetMode enumeration [SMI], smi.wcmtargetmode, wcmconfig/OfflineMode, wcmconfig/OnlineMode, wcmconfig/WcmTargetMode
ms.topic: enum
f1_keywords: ["wcmconfig/WcmTargetMode"]
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
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
 - WcmConfig.h
api_name:
 - WcmTargetMode
product: Windows
targetos: Windows
req.typenames: WcmTargetMode
req.redist: 
ms.custom: 19H1
---

# WcmTargetMode enumeration


## -description


Enumerates the various target modes. A target mode identifies how the redirections, from the target, are handled.


## -enum-fields




### -field OfflineMode

This value indicates that the only expansions that will be performed on environment variables are those defined in the target.


### -field OnlineMode

This value indicates that the expansions will preferentially expand from the target. If a matching expansion is not found, the expansions will fall through to the current environment of the process.

