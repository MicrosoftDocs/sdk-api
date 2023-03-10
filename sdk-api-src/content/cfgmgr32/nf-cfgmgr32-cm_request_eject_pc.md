---
UID: NF:cfgmgr32.CM_Request_Eject_PC
title: CM_Request_Eject_PC function (cfgmgr32.h)
description: The CM_Request_Eject_PC function requests that a portable PC, which is inserted in a local docking station, be ejected.
helpviewer_keywords: ["CM_Request_Eject_PC","CM_Request_Eject_PC function [Device and Driver Installation]","cfgmgr32/CM_Request_Eject_PC","cfgmgrfn_b5855f88-c1d1-432e-bac2-ffe6a728418e.xml","devinst.cm_request_eject_pc"]
old-location: devinst\cm_request_eject_pc.htm
tech.root: devinst
ms.assetid: 45d8151a-67d0-4cb1-8593-4cfb271a3411
ms.date: 12/05/2018
ms.keywords: CM_Request_Eject_PC, CM_Request_Eject_PC function [Device and Driver Installation], cfgmgr32/CM_Request_Eject_PC, cfgmgrfn_b5855f88-c1d1-432e-bac2-ffe6a728418e.xml, devinst.cm_request_eject_pc
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_Request_Eject_PC
 - cfgmgr32/CM_Request_Eject_PC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Request_Eject_PC
---

# CM_Request_Eject_PC function


## -description

The <b>CM_Request_Eject_PC</b> function requests that a portable PC, which is inserted in a local <a href="/windows-hardware/drivers/">docking station</a>, be ejected.



## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

Use this function to request that a portable PC, which is inserted in a local docking station, be ejected. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a> identifies whether a docking station is present in a local machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a> identifies whether a docking station is present in a local or a remote machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a>
