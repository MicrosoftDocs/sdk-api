---
UID: NF:gpmgmt.IGPMSOM.SetSecurityInfo
title: IGPMSOM::SetSecurityInfo (gpmgmt.h)
description: Sets the list of permissions for the scope of management (SOM) to that of the specified object.
helpviewer_keywords: ["GPMSOM class [GPMC]","SetSecurityInfo method","IGPMSOM interface [GPMC]","SetSecurityInfo method","IGPMSOM.SetSecurityInfo","IGPMSOM::SetSecurityInfo","SetSecurityInfo","SetSecurityInfo method [GPMC]","SetSecurityInfo method [GPMC]","GPMSOM class","SetSecurityInfo method [GPMC]","IGPMSOM interface","_win32_igpmsom_setsecurityinfo","gpmc.igpmsom_setsecurityinfo","gpmgmt/IGPMSOM::SetSecurityInfo"]
old-location: gpmc\igpmsom_setsecurityinfo.htm
tech.root: gpmc
ms.assetid: 675de64c-4eef-47c8-a06c-9167559b11a9
ms.date: 12/05/2018
ms.keywords: GPMSOM class [GPMC],SetSecurityInfo method, IGPMSOM interface [GPMC],SetSecurityInfo method, IGPMSOM.SetSecurityInfo, IGPMSOM::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMSOM class, SetSecurityInfo method [GPMC],IGPMSOM interface, _win32_igpmsom_setsecurityinfo, gpmc.igpmsom_setsecurityinfo, gpmgmt/IGPMSOM::SetSecurityInfo
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
 - IGPMSOM::SetSecurityInfo
 - gpmgmt/IGPMSOM::SetSecurityInfo
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
 - IGPMSOM.SetSecurityInfo
 - GPMSOM.SetSecurityInfo
---

## -description

Sets the list of permissions for the scope of management (SOM) to that of the specified object.

## -parameters

### -param pSecurityInfo [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>