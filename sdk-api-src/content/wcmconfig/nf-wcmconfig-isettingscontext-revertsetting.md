---
UID: NF:wcmconfig.ISettingsContext.RevertSetting
title: ISettingsContext::RevertSetting (wcmconfig.h)
author: windows-sdk-content
description: Reverts a setting in the namespace.
old-location: smi\isettingscontext_revertsetting.htm
tech.root: SMI
ms.assetid: 11f541e6-fd97-4756-91c1-44ba2e3d35b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISettingsContext interface [SMI],RevertSetting method, ISettingsContext.RevertSetting, ISettingsContext::RevertSetting, RevertSetting, RevertSetting method [SMI], RevertSetting method [SMI],ISettingsContext interface, smi.isettingscontext_revertsetting, wcmconfig/ISettingsContext::RevertSetting
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
 - ISettingsContext.RevertSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISettingsContext::RevertSetting


## -description


Reverts a setting in the namespace.


## -parameters




### -param pIdentity [in]

The fully-specified identity for the namespace that holds the setting  to be reverted.


### -param pwzSetting [in]

A path to a setting within the namespace that has been overridden in this context.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if <i>pIdentity</i> specifies a namespace that is not currently in the context. It returns <b>WCM_E_STATENODENOTFOUND</b> if <i>pwzSetting</i> is not changed in the context.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

