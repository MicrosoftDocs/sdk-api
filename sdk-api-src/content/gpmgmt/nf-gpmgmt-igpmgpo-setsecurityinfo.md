---
UID: NF:gpmgmt.IGPMGPO.SetSecurityInfo
title: IGPMGPO::SetSecurityInfo (gpmgmt.h)
description: Sets the list of permissions for the group policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.
helpviewer_keywords: ["GPMGPO class [GPMC]","SetSecurityInfo method","IGPMGPO interface [GPMC]","SetSecurityInfo method","IGPMGPO.SetSecurityInfo","IGPMGPO::SetSecurityInfo","SetSecurityInfo","SetSecurityInfo method [GPMC]","SetSecurityInfo method [GPMC]","GPMGPO class","SetSecurityInfo method [GPMC]","IGPMGPO interface","_win32_igpmgpo_setsecurityinfo","gpmc.igpmgpo_setsecurityinfo","gpmgmt/IGPMGPO::SetSecurityInfo"]
old-location: gpmc\igpmgpo_setsecurityinfo.htm
tech.root: gpmc
ms.assetid: 52b55e05-6107-4fa7-9991-55550393fee5
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],SetSecurityInfo method, IGPMGPO interface [GPMC],SetSecurityInfo method, IGPMGPO.SetSecurityInfo, IGPMGPO::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],GPMGPO class, SetSecurityInfo method [GPMC],IGPMGPO interface, _win32_igpmgpo_setsecurityinfo, gpmc.igpmgpo_setsecurityinfo, gpmgmt/IGPMGPO::SetSecurityInfo
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
 - IGPMGPO::SetSecurityInfo
 - gpmgmt/IGPMGPO::SetSecurityInfo
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
 - IGPMGPO.SetSecurityInfo
 - GPMGPO.SetSecurityInfo
---

## -description

Sets the list of permissions for the group policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.

## -parameters

### -param pSecurityInfo [in]

Pointer to the security information to apply to the GPO.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>
