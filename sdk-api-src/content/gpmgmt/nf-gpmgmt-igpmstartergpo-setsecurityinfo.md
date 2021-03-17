---
UID: NF:gpmgmt.IGPMStarterGPO.SetSecurityInfo
title: IGPMStarterGPO::SetSecurityInfo (gpmgmt.h)
description: Sets the list of permissions for the Group Policy object (GPO).
helpviewer_keywords: ["IGPMStarterGPO interface [GPMC]","SetSecurityInfo method","IGPMStarterGPO.SetSecurityInfo","IGPMStarterGPO::SetSecurityInfo","SetSecurityInfo","SetSecurityInfo method [GPMC]","SetSecurityInfo method [GPMC]","IGPMStarterGPO interface","gpmc.igpmstartergpo_setsecurityinfo","gpmgmt/IGPMStarterGPO::SetSecurityInfo"]
old-location: gpmc\igpmstartergpo_setsecurityinfo.htm
tech.root: gpmc
ms.assetid: ad4df57f-29b3-4a18-922a-a0d4457703ad
ms.date: 12/05/2018
ms.keywords: IGPMStarterGPO interface [GPMC],SetSecurityInfo method, IGPMStarterGPO.SetSecurityInfo, IGPMStarterGPO::SetSecurityInfo, SetSecurityInfo, SetSecurityInfo method [GPMC], SetSecurityInfo method [GPMC],IGPMStarterGPO interface, gpmc.igpmstartergpo_setsecurityinfo, gpmgmt/IGPMStarterGPO::SetSecurityInfo
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
 - IGPMStarterGPO::SetSecurityInfo
 - gpmgmt/IGPMStarterGPO::SetSecurityInfo
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
 - IGPMStarterGPO.SetSecurityInfo
---

# IGPMStarterGPO::SetSecurityInfo


## -description

Sets the list of permissions for the Group Policy object (GPO), such as who is granted permission to edit it. The method replaces the existing list of permissions.

## -parameters

### -param pSecurityInfo [in]

Pointer to the security information to apply to the GPO.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>