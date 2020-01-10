---
UID: NF:comsvcs.IServiceSxsConfig.SxsName
title: IServiceSxsConfig::SxsName (comsvcs.h)
description: Sets the file name of the side-by-side assembly for the enclosed work.
old-location: cos\iservicesxsconfig_sxsname.htm
tech.root: cossdk
ms.assetid: 622632ba-1287-4303-a9dd-4fb870e43786
ms.date: 12/05/2018
ms.keywords: IServiceSxsConfig interface [COM+],SxsName method, IServiceSxsConfig.SxsName, IServiceSxsConfig::SxsName, SxsName, SxsName method [COM+], SxsName method [COM+],IServiceSxsConfig interface, _cos_IServiceSxsConfig_SxsName, comsvcs/IServiceSxsConfig::SxsName, cos.iservicesxsconfig_sxsname
f1_keywords:
- comsvcs/IServiceSxsConfig.SxsName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IServiceSxsConfig.SxsName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceSxsConfig::SxsName


## -description


Sets the file name of the side-by-side assembly for the enclosed work.


## -parameters




### -param szSxsName [in]

The file name for the side-by-side assembly.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The appropriate file name extension will be added to the <i>szSxsName</i> parameter. A default file name is used if this method is not called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicesxsconfig">IServiceSxsConfig</a>
 

 

