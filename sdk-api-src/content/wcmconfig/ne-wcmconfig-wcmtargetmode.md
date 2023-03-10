---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0001
title: WcmTargetMode (wcmconfig.h)
description: Enumerates the various target modes.
helpviewer_keywords: ["OfflineMode","OnlineMode","WcmTargetMode","WcmTargetMode enumeration [SMI]","smi.wcmtargetmode","wcmconfig/OfflineMode","wcmconfig/OnlineMode","wcmconfig/WcmTargetMode"]
old-location: smi\wcmtargetmode.htm
tech.root: SMI
ms.assetid: 7a3b61f4-c98f-4c59-98dd-b513f69ac7d8
ms.date: 12/05/2018
ms.keywords: OfflineMode, OnlineMode, WcmTargetMode, WcmTargetMode enumeration [SMI], smi.wcmtargetmode, wcmconfig/OfflineMode, wcmconfig/OnlineMode, wcmconfig/WcmTargetMode
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
targetos: Windows
req.typenames: WcmTargetMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0001
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0001
 - WcmTargetMode
 - wcmconfig/WcmTargetMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmTargetMode
---

# WcmTargetMode enumeration


## -description

Enumerates the various target modes. A target mode identifies how the redirections, from the target, are handled.

## -enum-fields

### -field OfflineMode:1

This value indicates that the only expansions that will be performed on environment variables are those defined in the target.

### -field OnlineMode:2

This value indicates that the expansions will preferentially expand from the target. If a matching expansion is not found, the expansions will fall through to the current environment of the process.

