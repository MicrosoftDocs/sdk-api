---
UID: NN:gpmgmt.IGPMTrustee
title: IGPMTrustee (gpmgmt.h)
description: The IGPMTrustee interface contains methods to retrieve information about a given trustee when using the Group Policy Management Console (GPMC).
helpviewer_keywords: ["GPMTrustee","IGPMTrustee","IGPMTrustee interface [GPMC]","IGPMTrustee interface [GPMC]","described","_win32_igpmtrustee","gpmc.igpmtrustee","gpmgmt/IGPMTrustee"]
old-location: gpmc\igpmtrustee.htm
tech.root: gpmc
ms.assetid: f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb
ms.date: 12/05/2018
ms.keywords: GPMTrustee, IGPMTrustee, IGPMTrustee interface [GPMC], IGPMTrustee interface [GPMC],described, _win32_igpmtrustee, gpmc.igpmtrustee, gpmgmt/IGPMTrustee
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
 - IGPMTrustee
 - gpmgmt/IGPMTrustee
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
 - IGPMTrustee
 - GPMTrustee
---

# IGPMTrustee interface


## -description

The 
<b>IGPMTrustee</b> interface contains methods to retrieve information about a given trustee when using the Group Policy Management Console (GPMC). The <b>GPMTrustee</b> object represents a user, group or security group in the domain. To create a <b>GPMTrustee</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createtrustee">IGPM::CreateTrustee</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>