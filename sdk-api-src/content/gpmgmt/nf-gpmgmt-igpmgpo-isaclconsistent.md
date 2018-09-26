---
UID: NF:gpmgmt.IGPMGPO.IsACLConsistent
title: IGPMGPO::IsACLConsistent
author: windows-sdk-content
description: Checks for the consistency of ACLs between the Directory Service and the system volume folder (SysVol).
old-location: gpmc\igpmgpo_isaclconsistent.htm
tech.root: GPMC
ms.assetid: 4a4f2d87-bfaa-453a-9dbe-de19ba1d1953
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMGPO class [GPMC],IsACLConsistent method, IGPMGPO interface [GPMC],IsACLConsistent method, IGPMGPO.IsACLConsistent, IGPMGPO::IsACLConsistent, IsACLConsistent, IsACLConsistent method [GPMC], IsACLConsistent method [GPMC],GPMGPO class, IsACLConsistent method [GPMC],IGPMGPO interface, _win32_igpmgpo_isaclconsistent, gpmc.igpmgpo_isaclconsistent, gpmgmt/IGPMGPO::IsACLConsistent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMGPO::IsACLConsistent


## -description


Checks for the consistency of ACLs between the Directory Service and the system volume folder (SysVol).


## -parameters




### -param pvbConsistent [out]

Value that indicates whether the 
<a href="security.access_control_lists_acls_">access control lists (ACLs)</a> on the different parts of the GPO are consistent. If <b>VARIANT_TRUE</b>, they are consistent.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs or if the ACLs are not consistent.

<h3>JScript</h3>
Value that indicates whether the ACLs are consistent. If <b>VARIANT_TRUE</b>, they are consistent. For more information, see the following Remarks section.

<h3>VB</h3>
Value that indicates whether the ACLs are consistent. If <b>VARIANT_TRUE</b>, they are consistent. For more information, see the following Remarks section.




## -remarks



For more information about ACLs and the security model for controlling access to Windows objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 

