---
UID: NE:comsvcs.tagCSC_SxsConfig
title: CSC_SxsConfig (comsvcs.h)
description: Indicates how side-by-side assemblies are configured for CServiceConfig.helpviewer_keywords: ["CSC_InheritSxs","CSC_NewSxs","CSC_NoSxs","CSC_SxsConfig","CSC_SxsConfig enumeration [COM+]","_cos_CSC_SxsConfig","comsvcs/CSC_InheritSxs","comsvcs/CSC_NewSxs","comsvcs/CSC_NoSxs","comsvcs/CSC_SxsConfig","cos.csc_sxsconfig"]
old-location: cos\csc_sxsconfig.htm
tech.root: cossdk
ms.assetid: 8c114e9e-b201-4317-8a45-d5b0964c6ff8
ms.date: 12/05/2018
ms.keywords: CSC_InheritSxs, CSC_NewSxs, CSC_NoSxs, CSC_SxsConfig, CSC_SxsConfig enumeration [COM+], _cos_CSC_SxsConfig, comsvcs/CSC_InheritSxs, comsvcs/CSC_NewSxs, comsvcs/CSC_NoSxs, comsvcs/CSC_SxsConfig, cos.csc_sxsconfig
f1_keywords:
- comsvcs/CSC_SxsConfig
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
- HeaderDef
api_location:
- ComSvcs.h
api_name:
- CSC_SxsConfig
targetos: Windows
req.typenames: CSC_SxsConfig
req.redist: 
ms.custom: 19H1
---

# CSC_SxsConfig enumeration


## -description


Indicates how side-by-side assemblies are configured for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>.


## -enum-fields




### -field CSC_NoSxs

Side-by-side assemblies are not used within the enclosed context. This is the default setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritSxs

The current side-by-side assembly of the enclosed context is used. This is the default setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_NewSxs

A new side-by-side assembly is created for the enclosed context.


## -remarks



This enumeration is used to configure side-by-side assemblies through <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicesxsconfig">IServiceSxSConfig::SxSConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal">Isolated Applications and Side-by-side Assemblies</a>
 

 

