---
UID: NF:wcmconfig.ITargetInfo.SetModulePath
title: ITargetInfo::SetModulePath (wcmconfig.h)
description: Sets the module path for the offline installation location.
helpviewer_keywords: ["ITargetInfo interface [SMI]","SetModulePath method","ITargetInfo.SetModulePath","ITargetInfo::SetModulePath","SetModulePath","SetModulePath method [SMI]","SetModulePath method [SMI]","ITargetInfo interface","smi.itargetinfo_setmodulepath","wcmconfig/ITargetInfo::SetModulePath"]
old-location: smi\itargetinfo_setmodulepath.htm
tech.root: SMI
ms.assetid: 4831fdf9-411b-4fdb-bd5c-3a309e6b6918
ms.date: 12/05/2018
ms.keywords: ITargetInfo interface [SMI],SetModulePath method, ITargetInfo.SetModulePath, ITargetInfo::SetModulePath, SetModulePath, SetModulePath method [SMI], SetModulePath method [SMI],ITargetInfo interface, smi.itargetinfo_setmodulepath, wcmconfig/ITargetInfo::SetModulePath
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
 - ITargetInfo::SetModulePath
 - wcmconfig/ITargetInfo::SetModulePath
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
 - ITargetInfo.SetModulePath
---

# ITargetInfo::SetModulePath


## -description

Sets the module path for the offline installation location.

## -parameters

### -param Module [in]

The name of the module.

### -param Path [in]

The module path.

## -returns

This method returns an HRESULT value. <b>S_OK</b> indicates success.

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-itargetinfo">ITargetInfo</a>