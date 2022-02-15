---
UID: NF:gpmgmt.IGPMGPO.MakeACLConsistent
title: IGPMGPO::MakeACLConsistent (gpmgmt.h)
description: Makes ACLs consistent on the Directory Service and the system volume folder (SysVol) of the GPO. IsACLConsistent can be used to check for consistency of ACLs between the Directory Service and system volume folder (SysVol).
helpviewer_keywords: ["GPMGPO class [GPMC]","MakeACLConsistent method","IGPMGPO interface [GPMC]","MakeACLConsistent method","IGPMGPO.MakeACLConsistent","IGPMGPO::MakeACLConsistent","MakeACLConsistent","MakeACLConsistent method [GPMC]","MakeACLConsistent method [GPMC]","GPMGPO class","MakeACLConsistent method [GPMC]","IGPMGPO interface","gpmc.igpmgpo_makeaclconsistent","gpmgmt/IGPMGPO::MakeACLConsistent"]
old-location: gpmc\igpmgpo_makeaclconsistent.htm
tech.root: gpmc
ms.assetid: 936e7795-e5ab-4014-86df-6b74ab122b11
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],MakeACLConsistent method, IGPMGPO interface [GPMC],MakeACLConsistent method, IGPMGPO.MakeACLConsistent, IGPMGPO::MakeACLConsistent, MakeACLConsistent, MakeACLConsistent method [GPMC], MakeACLConsistent method [GPMC],GPMGPO class, MakeACLConsistent method [GPMC],IGPMGPO interface, gpmc.igpmgpo_makeaclconsistent, gpmgmt/IGPMGPO::MakeACLConsistent
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
 - IGPMGPO::MakeACLConsistent
 - gpmgmt/IGPMGPO::MakeACLConsistent
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
 - IGPMGPO.MakeACLConsistent
 - GPMGPO.MakeACLConsistent
---

# IGPMGPO::MakeACLConsistent


## -description

Makes <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> consistent on the Directory Service and the system  volume folder (SysVol) of the GPO. <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-isaclconsistent">IsACLConsistent</a> can be used to check for consistency of ACLs between the Directory Service and system volume folder (SysVol).



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

For more information about ACLs and the security model for controlling access to Windows objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-isaclconsistent">IGPMGPO::IsACLConsistent</a>
