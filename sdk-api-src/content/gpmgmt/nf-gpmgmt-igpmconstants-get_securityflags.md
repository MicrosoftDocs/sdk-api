---
UID: NF:gpmgmt.IGPMConstants.get_SecurityFlags
title: IGPMConstants::get_SecurityFlags (gpmgmt.h)
description: Retrieves the value of the SecurityFlags property, which represents the portion of the security descriptor to retrieve or set for a GPO.
helpviewer_keywords: ["GPMConstants object [GPMC]","SecurityFlags property","IGPMConstants interface [GPMC]","SecurityFlags property","IGPMConstants.SecurityFlags","IGPMConstants.get_SecurityFlags","IGPMConstants::SecurityFlags","IGPMConstants::get_SecurityFlags","SecurityFlags property [GPMC]","SecurityFlags property [GPMC]","GPMConstants object","SecurityFlags property [GPMC]","IGPMConstants interface","get_SecurityFlags","gpmc.igpmconstants_get_securityflags","gpmgmt/IGPMConstants::SecurityFlags","gpmgmt/IGPMConstants::get_SecurityFlags"]
old-location: gpmc\igpmconstants_get_securityflags.htm
tech.root: gpmc
ms.assetid: f9f950e1-b106-4907-a84a-ad20abfd02b1
ms.date: 12/05/2018
ms.keywords: GPMConstants object [GPMC],SecurityFlags property, IGPMConstants interface [GPMC],SecurityFlags property, IGPMConstants.SecurityFlags, IGPMConstants.get_SecurityFlags, IGPMConstants::SecurityFlags, IGPMConstants::get_SecurityFlags, SecurityFlags property [GPMC], SecurityFlags property [GPMC],GPMConstants object, SecurityFlags property [GPMC],IGPMConstants interface, get_SecurityFlags, gpmc.igpmconstants_get_securityflags, gpmgmt/IGPMConstants::SecurityFlags, gpmgmt/IGPMConstants::get_SecurityFlags
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
 - IGPMConstants::get_SecurityFlags
 - gpmgmt/IGPMConstants::get_SecurityFlags
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
 - IGPMConstants.SecurityFlags
 - IGPMConstants.get_SecurityFlags
 - GPMConstants.SecurityFlags
---

# IGPMConstants::get_SecurityFlags


## -description

Retrieves the value of the 
<b>SecurityFlags</b> property, which represents the portion of the security descriptor to retrieve or set for a GPO. You can pass the returned value in the <i>ulFlags</i> parameter to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-getsecuritydescriptor">IGPMGPO::GetSecurityDescriptor</a> and 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-setsecuritydescriptor">IGPMGPO::SetSecurityDescriptor</a> methods.

This property is read-only.

## -parameters

## -remarks

For more information about access control lists (ACLs) and the security model for controlling access to objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmconstants">IGPMConstants</a>