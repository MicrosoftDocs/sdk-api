---
UID: NF:comsvcs.ICheckSxsConfig.IsSameSxsConfig
title: ICheckSxsConfig::IsSameSxsConfig (comsvcs.h)
description: Determines whether the side-by-side assembly has the specified configuration.
helpviewer_keywords: ["ICheckSxsConfig interface [COM+]","IsSameSxsConfig method","ICheckSxsConfig.IsSameSxsConfig","ICheckSxsConfig::IsSameSxsConfig","IsSameSxsConfig","IsSameSxsConfig method [COM+]","IsSameSxsConfig method [COM+]","ICheckSxsConfig interface","_cos_ICheckSxsConfig_IsSameSxsConfig","comsvcs/ICheckSxsConfig::IsSameSxsConfig","cos.ichecksxsconfig_issamesxsconfig"]
old-location: cos\ichecksxsconfig_issamesxsconfig.htm
tech.root: cos
ms.assetid: 24ea3b88-2364-49e9-88cf-90a6094b9e4c
ms.date: 12/05/2018
ms.keywords: ICheckSxsConfig interface [COM+],IsSameSxsConfig method, ICheckSxsConfig.IsSameSxsConfig, ICheckSxsConfig::IsSameSxsConfig, IsSameSxsConfig, IsSameSxsConfig method [COM+], IsSameSxsConfig method [COM+],ICheckSxsConfig interface, _cos_ICheckSxsConfig_IsSameSxsConfig, comsvcs/ICheckSxsConfig::IsSameSxsConfig, cos.ichecksxsconfig_issamesxsconfig
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICheckSxsConfig::IsSameSxsConfig
 - comsvcs/ICheckSxsConfig::IsSameSxsConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICheckSxsConfig.IsSameSxsConfig
---

# ICheckSxsConfig::IsSameSxsConfig


## -description

Determines whether the side-by-side assembly has the specified configuration.

## -parameters

### -param wszSxsName [in]

A text string that contains the file name of the side-by-side assembly. The proper extension is added automatically.

### -param wszSxsDirectory [in]

A text string that contains the directory of the side-by-side assembly.

### -param wszSxsAppName [in]

A text string that contains the name of the application domain.

## -returns

This method can return the standard return values E_INVALIDARG and E_OUTOFMEMORY, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The current side-by-side assembly has the specified configuration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The current side-by-side assembly does not have the specified configuration.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-ichecksxsconfig">ICheckSxsConfig</a>