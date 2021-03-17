---
UID: NF:gpmgmt.IGPMClientSideExtension.IsComputerEnabled
title: IGPMClientSideExtension::IsComputerEnabled (gpmgmt.h)
description: Checks whether the client-side extension can be called during the processing of computer policy.
helpviewer_keywords: ["GPMClientSideExtension object [GPMC]","IsComputerEnabled method","IGPMClientSideExtension interface [GPMC]","IsComputerEnabled method","IGPMClientSideExtension.IsComputerEnabled","IGPMClientSideExtension::IsComputerEnabled","IsComputerEnabled","IsComputerEnabled method [GPMC]","IsComputerEnabled method [GPMC]","GPMClientSideExtension object","IsComputerEnabled method [GPMC]","IGPMClientSideExtension interface","_win32_igpmclientsideextension_iscomputerenabled","gpmc.igpmclientsideextension_iscomputerenabled","gpmgmt/IGPMClientSideExtension::IsComputerEnabled"]
old-location: gpmc\igpmclientsideextension_iscomputerenabled.htm
tech.root: gpmc
ms.assetid: c15ca1b0-f744-426e-a54f-402eef461227
ms.date: 12/05/2018
ms.keywords: GPMClientSideExtension object [GPMC],IsComputerEnabled method, IGPMClientSideExtension interface [GPMC],IsComputerEnabled method, IGPMClientSideExtension.IsComputerEnabled, IGPMClientSideExtension::IsComputerEnabled, IsComputerEnabled, IsComputerEnabled method [GPMC], IsComputerEnabled method [GPMC],GPMClientSideExtension object, IsComputerEnabled method [GPMC],IGPMClientSideExtension interface, _win32_igpmclientsideextension_iscomputerenabled, gpmc.igpmclientsideextension_iscomputerenabled, gpmgmt/IGPMClientSideExtension::IsComputerEnabled
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMClientSideExtension::IsComputerEnabled
 - gpmgmt/IGPMClientSideExtension::IsComputerEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMClientSideExtension.IsComputerEnabled
 - GPMClientSideExtension.IsComputerEnabled
---

# IGPMClientSideExtension::IsComputerEnabled


## -description

Checks whether the client-side extension can be called during the processing of computer policy.

## -parameters

### -param pvbEnabled [out]

Value that indicates whether the client-side extension can be called during the processing of computer policy. If <b>VARIANT_TRUE</b>, the client-side extension is called during the processing of computer policy, provided that there are policy settings for the client-side extension in the computer portion of one or more of the applied GPOs.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the client-side extension can be configured in the computer portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.

<h3>VB</h3>
Value that indicates whether the client-side extension can be configured in the computer portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmclientsideextension">IGPMClientSideExtension</a>