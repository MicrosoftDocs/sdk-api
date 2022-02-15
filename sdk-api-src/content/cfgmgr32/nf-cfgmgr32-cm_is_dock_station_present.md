---
UID: NF:cfgmgr32.CM_Is_Dock_Station_Present
title: CM_Is_Dock_Station_Present function (cfgmgr32.h)
description: The CM_Is_Dock_Station_Present function identifies whether a docking station is present in a local machine.
helpviewer_keywords: ["CM_Is_Dock_Station_Present","CM_Is_Dock_Station_Present function [Device and Driver Installation]","cfgmgr32/CM_Is_Dock_Station_Present","cfgmgrfn_ad4a7b33-0c70-4f03-91e2-c4707c83656e.xml","devinst.cm_is_dock_station_present"]
old-location: devinst\cm_is_dock_station_present.htm
tech.root: devinst
ms.assetid: 1c07dca9-5209-46d5-a0a3-87a615e3d40a
ms.date: 12/05/2018
ms.keywords: CM_Is_Dock_Station_Present, CM_Is_Dock_Station_Present function [Device and Driver Installation], cfgmgr32/CM_Is_Dock_Station_Present, cfgmgrfn_ad4a7b33-0c70-4f03-91e2-c4707c83656e.xml, devinst.cm_is_dock_station_present
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
 - CM_Is_Dock_Station_Present
 - cfgmgr32/CM_Is_Dock_Station_Present
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
 - CM_Is_Dock_Station_Present
---

# CM_Is_Dock_Station_Present function


## -description

The <b>CM_Is_Dock_Station_Present</b> function identifies whether a <a href="/windows-hardware/drivers/">docking station</a> is present in a local machine.

## -parameters

### -param pbPresent [out]

Pointer to a Boolean value that indicates whether a docking station is present in a local machine. The function sets *<i>pbPresent</i> to <b>TRUE</b> if a docking station is present. Otherwise, the function sets *<i>pbPresent</i> to <b>FALSE</b>.

## -returns

If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.

## -remarks

Use this function to determine whether a docking station is present in a local machine. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a> identifies whether a docking station is present in a local or a remote machine.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
<li>

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex">CM_Is_Dock_Station_Present_Ex</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc">CM_Request_Eject_PC</a>



<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex">CM_Request_Eject_PC_Ex</a>