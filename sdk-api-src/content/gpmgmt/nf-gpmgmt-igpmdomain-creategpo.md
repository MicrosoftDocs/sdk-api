---
UID: NF:gpmgmt.IGPMDomain.CreateGPO
title: IGPMDomain::CreateGPO (gpmgmt.h)
description: Creates and retrieves a GPMGPO object with a default display name. Typically, the caller sets the display name immediately after calling this method.
helpviewer_keywords: ["CreateGPO","CreateGPO method [GPMC]","CreateGPO method [GPMC]","GPMDomain object","CreateGPO method [GPMC]","IGPMDomain interface","GPMDomain object [GPMC]","CreateGPO method","IGPMDomain interface [GPMC]","CreateGPO method","IGPMDomain.CreateGPO","IGPMDomain::CreateGPO","_win32_igpmdomain_creategpo","gpmc.igpmdomain_creategpo","gpmgmt/IGPMDomain::CreateGPO"]
old-location: gpmc\igpmdomain_creategpo.htm
tech.root: gpmc
ms.assetid: 00e83637-820b-488e-abf4-4210ac3b98b6
ms.date: 12/05/2018
ms.keywords: CreateGPO, CreateGPO method [GPMC], CreateGPO method [GPMC],GPMDomain object, CreateGPO method [GPMC],IGPMDomain interface, GPMDomain object [GPMC],CreateGPO method, IGPMDomain interface [GPMC],CreateGPO method, IGPMDomain.CreateGPO, IGPMDomain::CreateGPO, _win32_igpmdomain_creategpo, gpmc.igpmdomain_creategpo, gpmgmt/IGPMDomain::CreateGPO
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
 - IGPMDomain::CreateGPO
 - gpmgmt/IGPMDomain::CreateGPO
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
 - IGPMDomain.CreateGPO
 - GPMDomain.CreateGPO
---

# IGPMDomain::CreateGPO


## -description

Creates and retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object with a default display name. Typically, the caller sets the display name immediately after calling this method.

## -parameters

### -param ppNewGPO [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMGPO</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMGPO</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>