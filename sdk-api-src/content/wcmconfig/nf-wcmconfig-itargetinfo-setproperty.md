---
UID: NF:wcmconfig.ITargetInfo.SetProperty
title: ITargetInfo::SetProperty (wcmconfig.h)
description: Sets a property value for the offline installation location.
helpviewer_keywords: ["ITargetInfo interface [SMI]","SetProperty method","ITargetInfo.SetProperty","ITargetInfo::SetProperty","SetProperty","SetProperty method [SMI]","SetProperty method [SMI]","ITargetInfo interface","smi.itargetinfo_setproperty","wcmconfig/ITargetInfo::SetProperty"]
old-location: smi\itargetinfo_setproperty.htm
tech.root: SMI
ms.assetid: ecd93710-a9e8-41cf-b30c-97d1efe0fa6f
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetProperty method, ITargetInfo.SetProperty, ITargetInfo::SetProperty, SetProperty, SetProperty method [SMI], SetProperty method [SMI],ITargetInfo interface, smi.itargetinfo_setproperty, wcmconfig/ITargetInfo::SetProperty
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
 - ITargetInfo::SetProperty
 - wcmconfig/ITargetInfo::SetProperty
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
 - ITargetInfo.SetProperty
---

# ITargetInfo::SetProperty


## -description

Sets a property value for the offline installation location.

## -parameters

### -param Offline [in]

<b>True</b> if installation location is offline.

### -param Property [in]

The name of the property.

### -param Value [in]

The value of the property.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>