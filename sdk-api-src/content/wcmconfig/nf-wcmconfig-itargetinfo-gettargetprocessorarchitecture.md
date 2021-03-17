---
UID: NF:wcmconfig.ITargetInfo.GetTargetProcessorArchitecture
title: ITargetInfo::GetTargetProcessorArchitecture (wcmconfig.h)
description: Gets processor architecture associated with the current target.
helpviewer_keywords: ["GetTargetProcessorArchitecture","GetTargetProcessorArchitecture method [SMI]","GetTargetProcessorArchitecture method [SMI]","ITargetInfo interface","ITargetInfo interface [SMI]","GetTargetProcessorArchitecture method","ITargetInfo.GetTargetProcessorArchitecture","ITargetInfo::GetTargetProcessorArchitecture","smi.itargetinfo_gettargetprocessorarchitecture","wcmconfig/ITargetInfo::GetTargetProcessorArchitecture"]
old-location: smi\itargetinfo_gettargetprocessorarchitecture.htm
tech.root: SMI
ms.assetid: 7c66e131-97e6-4a8e-b4b0-927633d6d53a
ms.date: 12/05/2018
ms.keywords: GetTargetProcessorArchitecture, GetTargetProcessorArchitecture method [SMI], GetTargetProcessorArchitecture method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetTargetProcessorArchitecture method, ITargetInfo.GetTargetProcessorArchitecture, ITargetInfo::GetTargetProcessorArchitecture, smi.itargetinfo_gettargetprocessorarchitecture, wcmconfig/ITargetInfo::GetTargetProcessorArchitecture
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
 - ITargetInfo::GetTargetProcessorArchitecture
 - wcmconfig/ITargetInfo::GetTargetProcessorArchitecture
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
 - ITargetInfo.GetTargetProcessorArchitecture
---

# ITargetInfo::GetTargetProcessorArchitecture


## -description

Gets processor architecture associated with the current target.

## -parameters

### -param ProcessorArchitecture [out]

The processor architecture associated with the current target.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>