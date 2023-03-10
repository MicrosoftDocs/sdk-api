---
UID: NF:cfgmgr32.CM_Request_Eject_PC_Ex
title: CM_Request_Eject_PC_Ex function (cfgmgr32.h)
description: The CM_Request_Eject_PC_Ex function requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.
helpviewer_keywords: ["CM_Request_Eject_PC_Ex","CM_Request_Eject_PC_Ex function [Device and Driver Installation]","cfgmgr32/CM_Request_Eject_PC_Ex","cfgmgrfn_332d3bac-644d-407d-82e3-aa26af983184.xml","devinst.cm_request_eject_pc_ex"]
old-location: devinst\cm_request_eject_pc_ex.htm
tech.root: devinst
ms.assetid: 69bcbfa4-fb89-4b5f-bd0a-260569dfb466
ms.date: 12/05/2018
ms.keywords: CM_Request_Eject_PC_Ex, CM_Request_Eject_PC_Ex function [Device and Driver Installation], cfgmgr32/CM_Request_Eject_PC_Ex, cfgmgrfn_332d3bac-644d-407d-82e3-aa26af983184.xml, devinst.cm_request_eject_pc_ex
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
 - CM_Request_Eject_PC_Ex
 - cfgmgr32/CM_Request_Eject_PC_Ex
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
 - CM_Request_Eject_PC_Ex
---

# CM_Request_Eject_PC_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a> instead.]

The <b>CM_Request_Eject_PC_Ex</b> function requests that a portable PC, which is inserted in a local or a remote <a href="/windows-hardware/drivers/">docking station</a>, be ejected.

## -parameters

### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

Use this function to request that a portable PC, which is inserted in a local or a remote docking station, be ejected. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a> identifies whether a docking station is present in a local machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a> identifies whether a docking station is present in a local or a remote machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
</ul>
 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a>