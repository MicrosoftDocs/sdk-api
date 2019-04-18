---
UID: NF:wcmconfig.ISettingsContext.GetStoredSettings
title: ISettingsContext::GetStoredSettings (wcmconfig.h)
author: windows-sdk-content
description: Gets the stored setting changes from the context for the given namespace.
old-location: smi\isettingscontext_getstoredsettings.htm
tech.root: SMI
ms.assetid: 29ec0b36-31f2-4078-b1a4-872a8ed340e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStoredSettings, GetStoredSettings method [SMI], GetStoredSettings method [SMI],ISettingsContext interface, ISettingsContext interface [SMI],GetStoredSettings method, ISettingsContext.GetStoredSettings, ISettingsContext::GetStoredSettings, smi.isettingscontext_getstoredsettings, wcmconfig/ISettingsContext::GetStoredSettings
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
 - ISettingsContext.GetStoredSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsContext::GetStoredSettings


## -description


Gets the stored setting changes from the context for the given namespace. This method returns a pointer to an address of an enumerator for each of the parameters <i>ppAddedSettings</i>, <i>ppModifiedSettings</i>, and <i>ppDeletedSettings</i> that identifies the set of paths for the added, modified, and deleted settings respectively. These strings may then be passed to <a href="https://msdn.microsoft.com/11f541e6-fd97-4756-91c1-44ba2e3d35b1">ISettingsContext::RevertSetting</a>.


## -parameters




### -param pIdentity [in]

The <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> object that specifies the namespace to get the settings for. This namespace identity should be fully-specified.


### -param ppAddedSettings [out]

 A pointer to a newly allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the added settings. Each path identifies a setting added to the context. 


### -param ppModifiedSettings [out]

A pointer to a newly-allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the modified settings.


### -param ppDeletedSettings [out]

A pointer to a newly-allocated <a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a> object that lists the set of paths for the deleted settings.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_NAMESPACENOTFOUND</b> if <i>pIdentity</i> references a namespace that is not in the context.

It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources on the system to allocate the enumerators.




## -remarks



<i>ppAddedSettings</i>, <i>ppModifiedSettings</i>, and <i>ppDeletedSettings</i> are enumerators for which Current returns a var with variable type BSTR that identifies the paths for the added, modified, and deleted settings respectively. Enumerating through the enumerators produces a set of path strings, each of which identifies a setting that has been added, modified, or deleted in this context. These strings can then be passed to <a href="https://msdn.microsoft.com/11f541e6-fd97-4756-91c1-44ba2e3d35b1">RevertSetting</a>.




## -see-also




<a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a>
 

 

