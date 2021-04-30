---
UID: NF:gpmgmt.IGPMSOM.CreateGPOLink
title: IGPMSOM::CreateGPOLink (gpmgmt.h)
description: Links the specified GPO to the specified position in the list of GPOs that are linked to a particular SOM.
helpviewer_keywords: ["CreateGPOLink","CreateGPOLink method [GPMC]","CreateGPOLink method [GPMC]","GPMSOM class","CreateGPOLink method [GPMC]","IGPMSOM interface","GPMSOM class [GPMC]","CreateGPOLink method","IGPMSOM interface [GPMC]","CreateGPOLink method","IGPMSOM.CreateGPOLink","IGPMSOM::CreateGPOLink","_win32_igpmsom_creategpolink","gpmc.igpmsom_creategpolink","gpmgmt/IGPMSOM::CreateGPOLink"]
old-location: gpmc\igpmsom_creategpolink.htm
tech.root: gpmc
ms.assetid: 2f3d8234-617f-4ce4-846a-476c28251989
ms.date: 12/05/2018
ms.keywords: CreateGPOLink, CreateGPOLink method [GPMC], CreateGPOLink method [GPMC],GPMSOM class, CreateGPOLink method [GPMC],IGPMSOM interface, GPMSOM class [GPMC],CreateGPOLink method, IGPMSOM interface [GPMC],CreateGPOLink method, IGPMSOM.CreateGPOLink, IGPMSOM::CreateGPOLink, _win32_igpmsom_creategpolink, gpmc.igpmsom_creategpolink, gpmgmt/IGPMSOM::CreateGPOLink
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
 - IGPMSOM::CreateGPOLink
 - gpmgmt/IGPMSOM::CreateGPOLink
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
 - IGPMSOM.CreateGPOLink
 - GPMSOM.CreateGPOLink
---

## -description

Links the specified GPO to the specified position in the list of GPOs that are linked to a particular SOM. If another GPO link occupies the specified position, the method inserts the new link ahead of the older link, and moves the older link, and all subsequent links in the list, down by one.

## -parameters

### -param lLinkPos [in]

Position in which the GPO should be linked. The position is 1-based. If this parameter is – 1, the GPO is appended to the end of the list. If the position specified is greater than the current number of GPO links, the method fails and returns <b>E_INVALIDARG</b>.

### -param pGPO [in]

GPO to link.

### -param ppNewGPOLink [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolink">IGPMGPOLink</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMGPOLink</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMGPOLink</b> object.

## -remarks

Attempting to link a GPO to a particular SOM multiple times causes the method to fail with <b>ERROR_ALREADY_EXISTS</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpolink">IGPMGPOLink</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>