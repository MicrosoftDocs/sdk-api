---
UID: NF:wcmconfig.ISettingsIdentity.SetAttribute
title: ISettingsIdentity::SetAttribute (wcmconfig.h)
author: windows-sdk-content
description: Sets an identity attribute for a namespace identity.
old-location: smi\isettingsidentity_setattribute.htm
tech.root: SMI
ms.assetid: 498bb364-3da8-456d-8e77-22b508516de0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISettingsIdentity interface [SMI],SetAttribute method, ISettingsIdentity.SetAttribute, ISettingsIdentity::SetAttribute, SetAttribute, SetAttribute method [SMI], SetAttribute method [SMI],ISettingsIdentity interface, smi.isettingsidentity_setattribute, wcmconfig/ISettingsIdentity::SetAttribute
ms.topic: method
f1_keywords: 
 - "wcmconfig/ISettingsIdentity.SetAttribute"
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
 - ISettingsIdentity.SetAttribute
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsIdentity::SetAttribute


## -description


Sets an identity attribute for a namespace identity.


## -parameters




### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param Name [in]

The name of the attribute.


### -param Value [in]

The value of the attribute.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_ATTRIBUTENOTALLOWED</b> if the attribute specified by Name is not recognized.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a>
 

 

