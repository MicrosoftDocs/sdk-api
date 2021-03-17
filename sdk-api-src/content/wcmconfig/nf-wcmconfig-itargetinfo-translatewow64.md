---
UID: NF:wcmconfig.ITargetInfo.TranslateWow64
title: ITargetInfo::TranslateWow64 (wcmconfig.h)
description: Translates paths for wow64 redirection.
helpviewer_keywords: ["ITargetInfo interface [SMI]","TranslateWow64 method","ITargetInfo.TranslateWow64","ITargetInfo::TranslateWow64","TranslateWow64","TranslateWow64 method [SMI]","TranslateWow64 method [SMI]","ITargetInfo interface","smi.itargetinfo_translatewow64","wcmconfig/ITargetInfo::TranslateWow64"]
old-location: smi\itargetinfo_translatewow64.htm
tech.root: SMI
ms.assetid: 0325bac8-1843-4e32-97a6-fb6e2bef9e16
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],TranslateWow64 method, ITargetInfo.TranslateWow64, ITargetInfo::TranslateWow64, TranslateWow64, TranslateWow64 method [SMI], TranslateWow64 method [SMI],ITargetInfo interface, smi.itargetinfo_translatewow64, wcmconfig/ITargetInfo::TranslateWow64
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
 - ITargetInfo::TranslateWow64
 - wcmconfig/ITargetInfo::TranslateWow64
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
 - ITargetInfo.TranslateWow64
---

# ITargetInfo::TranslateWow64


## -description

Translates paths for wow64 redirection.

## -parameters

### -param ClientArchitecture [in]

The name of the client architecture.

### -param Value [in]

The original path value.

### -param TranslatedValue [out]

The translated path value.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -remarks

<div class="alert"><b>Note</b>  This method is for internal use.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>