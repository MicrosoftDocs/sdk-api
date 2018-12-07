---
UID: NF:gpmgmt.IGPMConstants.get_SecurityFlags
title: IGPMConstants::get_SecurityFlags
author: windows-sdk-content
description: Retrieves the value of the SecurityFlags property, which represents the portion of the security descriptor to retrieve or set for a GPO.
old-location: gpmc\igpmconstants_get_securityflags.htm
tech.root: gpmc
ms.assetid: f9f950e1-b106-4907-a84a-ad20abfd02b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPMConstants object [GPMC],SecurityFlags property, IGPMConstants interface [GPMC],SecurityFlags property, IGPMConstants.SecurityFlags, IGPMConstants.get_SecurityFlags, IGPMConstants::SecurityFlags, IGPMConstants::get_SecurityFlags, SecurityFlags property [GPMC], SecurityFlags property [GPMC],GPMConstants object, SecurityFlags property [GPMC],IGPMConstants interface, get_SecurityFlags, gpmc.igpmconstants_get_securityflags, gpmgmt/IGPMConstants::SecurityFlags, gpmgmt/IGPMConstants::get_SecurityFlags
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
 - IGPMConstants.SecurityFlags
 - IGPMConstants.get_SecurityFlags
 - GPMConstants.SecurityFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMConstants::get_SecurityFlags


## -description


Retrieves the value of the 
<b>SecurityFlags</b> property, which represents the portion of the security descriptor to retrieve or set for a GPO. You can pass the returned value in the <i>ulFlags</i> parameter to the 
<a href="https://msdn.microsoft.com/4035119b-2688-4326-8d08-825d53c3d8e2">IGPMGPO::GetSecurityDescriptor</a> and 
<a href="https://msdn.microsoft.com/087cbe19-25d9-4134-8893-1b2906915220">IGPMGPO::SetSecurityDescriptor</a> methods.

This property is read-only.


## -parameters


## -remarks



For more information about access control lists (ACLs) and the security model for controlling access to objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">IGPMConstants</a>
 

 

