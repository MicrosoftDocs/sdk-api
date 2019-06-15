---
UID: NF:wcmconfig.ISettingsEngine.ApplySettingsContext
title: ISettingsEngine::ApplySettingsContext (wcmconfig.h)
author: windows-sdk-content
description: Applies a settings context.
old-location: smi\isettingsengine_applysettingscontext.htm
tech.root: SMI
ms.assetid: 459a97fb-e5fb-42a5-998d-84631fec2e6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplySettingsContext, ApplySettingsContext method [SMI], ApplySettingsContext method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],ApplySettingsContext method, ISettingsEngine.ApplySettingsContext, ISettingsEngine::ApplySettingsContext, smi.isettingsengine_applysettingscontext, wcmconfig/ISettingsEngine::ApplySettingsContext
ms.topic: method
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
 - ISettingsEngine.ApplySettingsContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsEngine::ApplySettingsContext


## -description


Applies a settings context.


## -parameters




### -param SettingsContext [in]

The context that contains the setting data to apply.


### -param pppwzIdentities [out]

Identities of the namespaces that were applied to the system in a string format.


### -param pcIdentities [out]

The number of identities in <i>pppwzIdentities</i>.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>
 

 

