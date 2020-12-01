---
UID: NF:gpmgmt.IGPMGPO.GetSecurityInfo
title: IGPMGPO::GetSecurityInfo (gpmgmt.h)
description: Retrieves the set of permissions for the GPO, such as who is granted permission to edit it.
helpviewer_keywords: ["GPMGPO class [GPMC]","GetSecurityInfo method","GetSecurityInfo","GetSecurityInfo method [GPMC]","GetSecurityInfo method [GPMC]","GPMGPO class","GetSecurityInfo method [GPMC]","IGPMGPO interface","IGPMGPO interface [GPMC]","GetSecurityInfo method","IGPMGPO.GetSecurityInfo","IGPMGPO::GetSecurityInfo","_win32_igpmgpo_getsecurityinfo","gpmc.igpmgpo_getsecurityinfo","gpmgmt/IGPMGPO::GetSecurityInfo"]
old-location: gpmc\igpmgpo_getsecurityinfo.htm
tech.root: gpmc
ms.assetid: 104e96e6-60c5-4cc1-9728-7c0ea9715a58
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],GetSecurityInfo method, GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],GPMGPO class, GetSecurityInfo method [GPMC],IGPMGPO interface, IGPMGPO interface [GPMC],GetSecurityInfo method, IGPMGPO.GetSecurityInfo, IGPMGPO::GetSecurityInfo, _win32_igpmgpo_getsecurityinfo, gpmc.igpmgpo_getsecurityinfo, gpmgmt/IGPMGPO::GetSecurityInfo
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
 - IGPMGPO::GetSecurityInfo
 - gpmgmt/IGPMGPO::GetSecurityInfo
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
 - IGPMGPO.GetSecurityInfo
 - GPMGPO.GetSecurityInfo
---

# IGPMGPO::GetSecurityInfo


## -description

Retrieves the set of permissions for the GPO, such as who is granted permission to edit it.

## -parameters

### -param ppSecurityInfo [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMSecurityInfo</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMSecurityInfo</b> object.

## -remarks

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>