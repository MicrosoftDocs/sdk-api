---
UID: NF:gpmgmt.IGPMDomain2.CreateStarterGPO
title: IGPMDomain2::CreateStarterGPO (gpmgmt.h)
description: Creates and retrieves a GPMStarterGPO object.
helpviewer_keywords: ["CreateStarterGPO","CreateStarterGPO method [GPMC]","CreateStarterGPO method [GPMC]","IGPMDomain2 interface","IGPMDomain2 interface [GPMC]","CreateStarterGPO method","IGPMDomain2.CreateStarterGPO","IGPMDomain2::CreateStarterGPO","gpmc.igpmdomain2_createstartergpo","gpmgmt/IGPMDomain2::CreateStarterGPO"]
old-location: gpmc\igpmdomain2_createstartergpo.htm
tech.root: gpmc
ms.assetid: 652ac85b-f488-4e27-81dd-1ffc5f9f42d6
ms.date: 12/05/2018
ms.keywords: CreateStarterGPO, CreateStarterGPO method [GPMC], CreateStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],CreateStarterGPO method, IGPMDomain2.CreateStarterGPO, IGPMDomain2::CreateStarterGPO, gpmc.igpmdomain2_createstartergpo, gpmgmt/IGPMDomain2::CreateStarterGPO
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
 - IGPMDomain2::CreateStarterGPO
 - gpmgmt/IGPMDomain2::CreateStarterGPO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMDomain2.CreateStarterGPO
---

# IGPMDomain2::CreateStarterGPO


## -description

Creates and retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object that has a default display name and description. Typically, the caller sets the display name and description immediately after calling this method. The Starter Group Policy object (GPO) ID is generated automatically.

## -parameters

### -param ppnewTemplate [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> interface.

## -returns

<h3>C++</h3>
 Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.



<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a>  object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a>  object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>