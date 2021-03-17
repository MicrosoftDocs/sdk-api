---
UID: NF:wcmconfig.ITargetInfo.SetWow64Context
title: ITargetInfo::SetWow64Context (wcmconfig.h)
description: Sets an opaque context object for wow64 redirection.
helpviewer_keywords: ["ITargetInfo interface [SMI]","SetWow64Context method","ITargetInfo.SetWow64Context","ITargetInfo::SetWow64Context","SetWow64Context","SetWow64Context method [SMI]","SetWow64Context method [SMI]","ITargetInfo interface","smi.itargetinfo_setwow64context","wcmconfig/ITargetInfo::SetWow64Context"]
old-location: smi\itargetinfo_setwow64context.htm
tech.root: SMI
ms.assetid: 8f44485d-0ad3-4c89-a1dc-19610f717972
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetWow64Context method, ITargetInfo.SetWow64Context, ITargetInfo::SetWow64Context, SetWow64Context, SetWow64Context method [SMI], SetWow64Context method [SMI],ITargetInfo interface, smi.itargetinfo_setwow64context, wcmconfig/ITargetInfo::SetWow64Context
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
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITargetInfo::SetWow64Context
 - wcmconfig/ITargetInfo::SetWow64Context
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.SetWow64Context
---

# ITargetInfo::SetWow64Context


## -description

Sets an opaque context object for wow64 redirection.

## -parameters

### -param InstallerModule [in]

The name of the installer module.

### -param Wow64Context [in]

The opaque context object for wow64 redirection.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>  This method is for internal use.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>