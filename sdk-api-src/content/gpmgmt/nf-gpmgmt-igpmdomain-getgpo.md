---
UID: NF:gpmgmt.IGPMDomain.GetGPO
title: IGPMDomain::GetGPO (gpmgmt.h)
description: Retrieves a GPMGPO object with a specified Group Policy object (GPO) ID. The group policy object ID is represented by a GUID.
helpviewer_keywords: ["GPMDomain object [GPMC]","GetGPO method","GetGPO","GetGPO method [GPMC]","GetGPO method [GPMC]","GPMDomain object","GetGPO method [GPMC]","IGPMDomain interface","IGPMDomain interface [GPMC]","GetGPO method","IGPMDomain.GetGPO","IGPMDomain::GetGPO","_win32_igpmdomain_getgpo","gpmc.igpmdomain_getgpo","gpmgmt/IGPMDomain::GetGPO"]
old-location: gpmc\igpmdomain_getgpo.htm
tech.root: gpmc
ms.assetid: ac413241-3649-4f22-9a67-94e4da8672e7
ms.date: 12/05/2018
ms.keywords: GPMDomain object [GPMC],GetGPO method, GetGPO, GetGPO method [GPMC], GetGPO method [GPMC],GPMDomain object, GetGPO method [GPMC],IGPMDomain interface, IGPMDomain interface [GPMC],GetGPO method, IGPMDomain.GetGPO, IGPMDomain::GetGPO, _win32_igpmdomain_getgpo, gpmc.igpmdomain_getgpo, gpmgmt/IGPMDomain::GetGPO
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
 - IGPMDomain::GetGPO
 - gpmgmt/IGPMDomain::GetGPO
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
 - IGPMDomain.GetGPO
 - GPMDomain.GetGPO
---

# IGPMDomain::GetGPO


## -description

Retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object with a specified Group Policy object (GPO) ID. The group policy object ID is represented by a GUID.

## -parameters

### -param bstrGuid [in]

Required. GUID representing the ID of the group policy object to access. Use null-terminated string.

### -param ppGPO [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface for the group policy object ID and domain specified.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>