---
UID: NF:gpmgmt.IGPMDomain2.GetStarterGPO
title: IGPMDomain2::GetStarterGPO (gpmgmt.h)
description: Retrieves a GPMStarterGPO object that has a specified Group Policy object ID.
helpviewer_keywords: ["GetStarterGPO","GetStarterGPO method [GPMC]","GetStarterGPO method [GPMC]","IGPMDomain2 interface","IGPMDomain2 interface [GPMC]","GetStarterGPO method","IGPMDomain2.GetStarterGPO","IGPMDomain2::GetStarterGPO","gpmc.igpmdomain2_getstartergpo","gpmgmt/IGPMDomain2::GetStarterGPO"]
old-location: gpmc\igpmdomain2_getstartergpo.htm
tech.root: gpmc
ms.assetid: 0648c653-94da-40d6-98c2-46f80a51bc90
ms.date: 12/05/2018
ms.keywords: GetStarterGPO, GetStarterGPO method [GPMC], GetStarterGPO method [GPMC],IGPMDomain2 interface, IGPMDomain2 interface [GPMC],GetStarterGPO method, IGPMDomain2.GetStarterGPO, IGPMDomain2::GetStarterGPO, gpmc.igpmdomain2_getstartergpo, gpmgmt/IGPMDomain2::GetStarterGPO
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
 - IGPMDomain2::GetStarterGPO
 - gpmgmt/IGPMDomain2::GetStarterGPO
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
 - IGPMDomain2.GetStarterGPO
---

# IGPMDomain2::GetStarterGPO


## -description

Retrieves a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object that has a specified Group Policy object ID. The GPO ID is represented by a GUID.

## -parameters

### -param bstrGuid [in]

Required. GUID that represents the ID of the GPO to access. Use a null-terminated string.

### -param ppTemplate [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a> interface for the specified Starter GPO ID.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">GPMStarterGPO</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain2">IGPMDomain2</a>