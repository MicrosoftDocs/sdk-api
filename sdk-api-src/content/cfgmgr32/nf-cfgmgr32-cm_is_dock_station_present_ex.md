---
UID: NF:cfgmgr32.CM_Is_Dock_Station_Present_Ex
title: CM_Is_Dock_Station_Present_Ex function (cfgmgr32.h)
description: The CM_Is_Dock_Station_Present_Ex function identifies whether a docking station is present in a local or a remote machine.
helpviewer_keywords: ["CM_Is_Dock_Station_Present_Ex","CM_Is_Dock_Station_Present_Ex function [Device and Driver Installation]","cfgmgr32/CM_Is_Dock_Station_Present_Ex","cfgmgrfn_9e17b4dc-d5ac-49fb-99f7-0fc1144e23f4.xml","devinst.cm_is_dock_station_present_ex"]
old-location: devinst\cm_is_dock_station_present_ex.htm
tech.root: devinst
ms.assetid: d94411e6-a98d-4feb-adfb-6d94e3d33d46
ms.date: 12/05/2018
ms.keywords: CM_Is_Dock_Station_Present_Ex, CM_Is_Dock_Station_Present_Ex function [Device and Driver Installation], cfgmgr32/CM_Is_Dock_Station_Present_Ex, cfgmgrfn_9e17b4dc-d5ac-49fb-99f7-0fc1144e23f4.xml, devinst.cm_is_dock_station_present_ex
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
 - CM_Is_Dock_Station_Present_Ex
 - cfgmgr32/CM_Is_Dock_Station_Present_Ex
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
 - CM_Is_Dock_Station_Present_Ex
---

# CM_Is_Dock_Station_Present_Ex function


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a> instead.]

The <b>CM_Is_Dock_Station_Present_Ex</b> function identifies whether a <a href="/windows-hardware/drivers/">docking station</a> is present in a local or a remote machine.

## -parameters

### -param pbPresent [out]

Pointer to a Boolean value that indicates whether a docking station is present in a local machine. The function sets *pbPresent to <b>TRUE</b> if a docking station is present. The function sets *<i>pbPresent</i> to <b>FALSE</b> if the function cannot connect to the specified machine or a docking station is not present.

### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

Use this function to determine whether a docking station is present in a local or a remote machine. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a> identifies whether a docking station is present in a local machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>
 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present">CM_Is_Dock_Station_Present</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a>