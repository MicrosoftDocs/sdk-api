---
UID: NF:gpmgmt.IGPMClientSideExtension.IsUserEnabled
title: IGPMClientSideExtension::IsUserEnabled (gpmgmt.h)
description: Checks whether the client-side extension can be called during the processing of user policy.
helpviewer_keywords: ["GPMClientSideExtension object [GPMC]","IsUserEnabled method","IGPMClientSideExtension interface [GPMC]","IsUserEnabled method","IGPMClientSideExtension.IsUserEnabled","IGPMClientSideExtension::IsUserEnabled","IsUserEnabled","IsUserEnabled method [GPMC]","IsUserEnabled method [GPMC]","GPMClientSideExtension object","IsUserEnabled method [GPMC]","IGPMClientSideExtension interface","_win32_igpmclientsideextension_isuserenabled","gpmc.igpmclientsideextension_isuserenabled","gpmgmt/IGPMClientSideExtension::IsUserEnabled"]
old-location: gpmc\igpmclientsideextension_isuserenabled.htm
tech.root: gpmc
ms.assetid: 01fba0fa-9639-4033-bbdf-704549524147
ms.date: 12/05/2018
ms.keywords: GPMClientSideExtension object [GPMC],IsUserEnabled method, IGPMClientSideExtension interface [GPMC],IsUserEnabled method, IGPMClientSideExtension.IsUserEnabled, IGPMClientSideExtension::IsUserEnabled, IsUserEnabled, IsUserEnabled method [GPMC], IsUserEnabled method [GPMC],GPMClientSideExtension object, IsUserEnabled method [GPMC],IGPMClientSideExtension interface, _win32_igpmclientsideextension_isuserenabled, gpmc.igpmclientsideextension_isuserenabled, gpmgmt/IGPMClientSideExtension::IsUserEnabled
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
 - IGPMClientSideExtension::IsUserEnabled
 - gpmgmt/IGPMClientSideExtension::IsUserEnabled
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
 - IGPMClientSideExtension.IsUserEnabled
 - GPMClientSideExtension.IsUserEnabled
---

# IGPMClientSideExtension::IsUserEnabled


## -description

Checks whether the client-side extension can be called during the processing of user policy.

## -parameters

### -param pvbEnabled [out]

Value that indicates whether the client-side extension can be called during the processing of user policy. If <b>VARIANT_TRUE</b>, the client-side extension is called during the processing of user policy, provided that there are policy settings for the client-side extension in the user portion of one or more of the applied GPOs.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the client-side extension can be configured in the user portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.

<h3>VB</h3>
Value that indicates whether the client-side extension can be configured in the user portion of the GPO. If <b>VARIANT_TRUE</b>, the client-side extension can be configured.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmclientsideextension">IGPMClientSideExtension</a>