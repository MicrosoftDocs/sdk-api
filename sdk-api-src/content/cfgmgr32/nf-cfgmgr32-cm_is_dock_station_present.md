---
UID: NF:cfgmgr32.CM_Is_Dock_Station_Present
title: CM_Is_Dock_Station_Present function
author: windows-sdk-content
description: The CM_Is_Dock_Station_Present function identifies whether a docking station is present in a local machine.
old-location: devinst\cm_is_dock_station_present.htm
tech.root: devinst
ms.assetid: 1c07dca9-5209-46d5-a0a3-87a615e3d40a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CM_Is_Dock_Station_Present, CM_Is_Dock_Station_Present function [Device and Driver Installation], cfgmgr32/CM_Is_Dock_Station_Present, cfgmgrfn_ad4a7b33-0c70-4f03-91e2-c4707c83656e.xml, devinst.cm_is_dock_station_present
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Is_Dock_Station_Present
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Is_Dock_Station_Present function


## -description


The <b>CM_Is_Dock_Station_Present</b> function identifies whether a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">docking station</a> is present in a local machine.


## -parameters




### -param pbPresent [out]

Pointer to a Boolean value that indicates whether a docking station is present in a local machine. The function sets *<i>pbPresen</i>t to <b>TRUE</b> if a docking station is present. Otherwise, the function sets *<i>pbPresen</i>t to <b>FALSE</b>.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



Use this function to determine whether a docking station is present in a local machine. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="https://msdn.microsoft.com/d94411e6-a98d-4feb-adfb-6d94e3d33d46">CM_Is_Dock_Station_Present_Ex</a> identifies whether a docking station is present in a local or a remote machine.

</li>
<li>

<a href="https://msdn.microsoft.com/45d8151a-67d0-4cb1-8593-4cfb271a3411">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
<li>

<a href="https://msdn.microsoft.com/69bcbfa4-fb89-4b5f-bd0a-260569dfb466">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/d94411e6-a98d-4feb-adfb-6d94e3d33d46">CM_Is_Dock_Station_Present_Ex</a>



<a href="https://msdn.microsoft.com/45d8151a-67d0-4cb1-8593-4cfb271a3411">CM_Request_Eject_PC</a>



<a href="https://msdn.microsoft.com/69bcbfa4-fb89-4b5f-bd0a-260569dfb466">CM_Request_Eject_PC_Ex</a>
 

 

