---
UID: NF:gpmgmt.IGPMStarterGPO.GetSecurityInfo
title: IGPMStarterGPO::GetSecurityInfo (gpmgmt.h)
description: Retrieves the set of permissions for the Starter GPO, such as who is granted permission to edit it.
helpviewer_keywords: ["GetSecurityInfo","GetSecurityInfo method [GPMC]","GetSecurityInfo method [GPMC]","IGPMStarterGPO interface","IGPMStarterGPO interface [GPMC]","GetSecurityInfo method","IGPMStarterGPO.GetSecurityInfo","IGPMStarterGPO::GetSecurityInfo","gpmc.igpmstartergpo_getsecurityinfo","gpmgmt/IGPMStarterGPO::GetSecurityInfo"]
old-location: gpmc\igpmstartergpo_getsecurityinfo.htm
tech.root: gpmc
ms.assetid: 5c411851-0902-454a-9b44-383ea572ab78
ms.date: 12/05/2018
ms.keywords: GetSecurityInfo, GetSecurityInfo method [GPMC], GetSecurityInfo method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],GetSecurityInfo method, IGPMStarterGPO.GetSecurityInfo, IGPMStarterGPO::GetSecurityInfo, gpmc.igpmstartergpo_getsecurityinfo, gpmgmt/IGPMStarterGPO::GetSecurityInfo
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
 - IGPMStarterGPO::GetSecurityInfo
 - gpmgmt/IGPMStarterGPO::GetSecurityInfo
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
 - IGPMStarterGPO.GetSecurityInfo
---

# IGPMStarterGPO::GetSecurityInfo


## -description

Retrieves the set of permissions for the Starter GPO, such as who is granted permission to edit it.

## -parameters

### -param ppSecurityInfo [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a> interface.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>