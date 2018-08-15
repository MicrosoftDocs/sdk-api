---
UID: NF:wcmconfig.ITargetInfo.TranslateWow64
title: ITargetInfo::TranslateWow64
author: windows-sdk-content
description: Translates paths for wow64 redirection.
old-location: smi\itargetinfo_translatewow64.htm
old-project: smi
ms.assetid: 0325bac8-1843-4e32-97a6-fb6e2bef9e16
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ITargetInfo interface [SMI],TranslateWow64 method, ITargetInfo.TranslateWow64, ITargetInfo::TranslateWow64, TranslateWow64, TranslateWow64 method [SMI], TranslateWow64 method [SMI],ITargetInfo interface, smi.itargetinfo_translatewow64, wcmconfig/ITargetInfo::TranslateWow64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.TranslateWow64
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

