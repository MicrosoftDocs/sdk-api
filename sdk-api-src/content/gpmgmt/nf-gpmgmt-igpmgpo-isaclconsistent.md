---
UID: NF:gpmgmt.IGPMGPO.IsACLConsistent
title: IGPMGPO::IsACLConsistent (gpmgmt.h)
description: Checks for the consistency of ACLs between the Directory Service and the system volume folder (SysVol).
helpviewer_keywords: ["GPMGPO class [GPMC]","IsACLConsistent method","IGPMGPO interface [GPMC]","IsACLConsistent method","IGPMGPO.IsACLConsistent","IGPMGPO::IsACLConsistent","IsACLConsistent","IsACLConsistent method [GPMC]","IsACLConsistent method [GPMC]","GPMGPO class","IsACLConsistent method [GPMC]","IGPMGPO interface","_win32_igpmgpo_isaclconsistent","gpmc.igpmgpo_isaclconsistent","gpmgmt/IGPMGPO::IsACLConsistent"]
old-location: gpmc\igpmgpo_isaclconsistent.htm
tech.root: gpmc
ms.assetid: 4a4f2d87-bfaa-453a-9dbe-de19ba1d1953
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],IsACLConsistent method, IGPMGPO interface [GPMC],IsACLConsistent method, IGPMGPO.IsACLConsistent, IGPMGPO::IsACLConsistent, IsACLConsistent, IsACLConsistent method [GPMC], IsACLConsistent method [GPMC],GPMGPO class, IsACLConsistent method [GPMC],IGPMGPO interface, _win32_igpmgpo_isaclconsistent, gpmc.igpmgpo_isaclconsistent, gpmgmt/IGPMGPO::IsACLConsistent
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
 - IGPMGPO::IsACLConsistent
 - gpmgmt/IGPMGPO::IsACLConsistent
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
 - IGPMGPO.IsACLConsistent
 - GPMGPO.IsACLConsistent
---

# IGPMGPO::IsACLConsistent


## -description

Checks for the consistency of ACLs between the Directory Service and the system volume folder (SysVol).

## -parameters

### -param pvbConsistent [out]

Value that indicates whether the 
<a href="/windows/desktop/SecAuthZ/access-control-lists">access control lists (ACLs)</a> on the different parts of the GPO are consistent. If <b>VARIANT_TRUE</b>, they are consistent.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs or if the ACLs are not consistent.

<h3>JScript</h3>
Value that indicates whether the ACLs are consistent. If <b>VARIANT_TRUE</b>, they are consistent. For more information, see the following Remarks section.

<h3>VB</h3>
Value that indicates whether the ACLs are consistent. If <b>VARIANT_TRUE</b>, they are consistent. For more information, see the following Remarks section.

## -remarks

For more information about ACLs and the security model for controlling access to Windows objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>