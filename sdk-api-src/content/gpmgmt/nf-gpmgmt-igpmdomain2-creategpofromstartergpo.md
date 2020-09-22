---
UID: NF:gpmgmt.IGPMDomain2.CreateGPOFromStarterGPO
title: IGPMDomain2::CreateGPOFromStarterGPO (gpmgmt.h)
description: Creates and retrieves a GPMGPO object from a GPMStarterGPO object.
helpviewer_keywords: ["CreateGPOFromStarterGPO","CreateGPOFromStarterGPO method [GPMC]","CreateGPOFromStarterGPO method [GPMC]","IGPMDomain2 interface","IGPMDomain2 interface [GPMC]","CreateGPOFromStarterGPO method","IGPMDomain2.CreateGPOFromStarterGPO","IGPMDomain2::CreateGPOFromStarterGPO","gpmc.igpmdomain2_creategpofromstartergpo","gpmgmt/IGPMDomain2::CreateGPOFromStarterGPO"]
old-location: gpmc\igpmdomain2_creategpofromstartergpo.htm
tech.root: gpmc
ms.assetid: 3a74f763-a9f5-4e93-94fb-7ef2a116c82b
ms.date: 12/05/2018
ms.keywords: CreateGPOFromStarterGPO, CreateGPOFromStarterGPO method [GPMC], CreateGPOFromStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],CreateGPOFromStarterGPO method, IGPMDomain2.CreateGPOFromStarterGPO, IGPMDomain2::CreateGPOFromStarterGPO, gpmc.igpmdomain2_creategpofromstartergpo, gpmgmt/IGPMDomain2::CreateGPOFromStarterGPO
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
 - IGPMDomain2::CreateGPOFromStarterGPO
 - gpmgmt/IGPMDomain2::CreateGPOFromStarterGPO
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
 - IGPMDomain2.CreateGPOFromStarterGPO
---

## -description

Creates and retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object from a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object. This method creates a new <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object. Then, this method copies the contents of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object into the <b>GPMGPO</b> object. Finally, this method updates the appropriate attributes of the <b>GPMGPO</b> object to reflect the configured data.

## -parameters

### -param pGPOTemplate [in]

A pointer to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object from which the new Group Policy object (GPO) will be created.

### -param ppnewGPO [out]

Address of a pointer to an <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object that represents the new GPO.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a>  object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a>  object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>