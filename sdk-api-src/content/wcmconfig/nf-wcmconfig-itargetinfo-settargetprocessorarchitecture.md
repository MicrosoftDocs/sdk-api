---
UID: NF:wcmconfig.ITargetInfo.SetTargetProcessorArchitecture
title: ITargetInfo::SetTargetProcessorArchitecture (wcmconfig.h)
author: windows-sdk-content
description: Sets the processor architecture associated with the current target.
old-location: smi\itargetinfo_settargetprocessorarchitecture.htm
tech.root: SMI
ms.assetid: 15056182-4355-48f5-b996-195e3c72235e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetTargetProcessorArchitecture method, ITargetInfo.SetTargetProcessorArchitecture, ITargetInfo::SetTargetProcessorArchitecture, SetTargetProcessorArchitecture, SetTargetProcessorArchitecture method [SMI], SetTargetProcessorArchitecture method [SMI],ITargetInfo interface, smi.itargetinfo_settargetprocessorarchitecture, wcmconfig/ITargetInfo::SetTargetProcessorArchitecture
ms.topic: method
f1_keywords: 
 - "wcmconfig/ITargetInfo.SetTargetProcessorArchitecture"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.SetTargetProcessorArchitecture
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITargetInfo::SetTargetProcessorArchitecture


## -description


Sets the processor architecture associated with the current target.


## -parameters




### -param ProcessorArchitecture [in]

The processor architecture associated with the current target.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. Returns <b>HRESULT_FROM_WIN32</b> (<b>ERROR_INVALID_OPERATION</b>) if the target processor architecture has been set. May return <b>E_OUTOFMEMORY</b> if system resources are low.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>
 

 

