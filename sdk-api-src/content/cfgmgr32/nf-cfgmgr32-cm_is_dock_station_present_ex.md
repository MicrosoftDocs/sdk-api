---
UID: NF:cfgmgr32.CM_Is_Dock_Station_Present_Ex
title: CM_Is_Dock_Station_Present_Ex function
author: windows-sdk-content
description: The CM_Is_Dock_Station_Present_Ex function identifies whether a docking station is present in a local or a remote machine.
old-location: devinst\cm_is_dock_station_present_ex.htm
tech.root: devinst
ms.assetid: d94411e6-a98d-4feb-adfb-6d94e3d33d46
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Is_Dock_Station_Present_Ex, CM_Is_Dock_Station_Present_Ex function [Device and Driver Installation], cfgmgr32/CM_Is_Dock_Station_Present_Ex, cfgmgrfn_9e17b4dc-d5ac-49fb-99f7-0fc1144e23f4.xml, devinst.cm_is_dock_station_present_ex
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
 - CM_Is_Dock_Station_Present_Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Is_Dock_Station_Present_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://msdn.microsoft.com/1c07dca9-5209-46d5-a0a3-87a615e3d40a">CM_Is_Dock_Station_Present</a> instead.]

The <b>CM_Is_Dock_Station_Present_Ex</b> function identifies whether a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">docking station</a> is present in a local or a remote machine.


## -parameters




### -param pbPresent [out]

Pointer to a Boolean value that indicates whether a docking station is present in a local machine. The function sets *pbPresent to <b>TRUE</b> if a docking station is present. The function sets *<i>pbPresent</i> to <b>FALSE</b> if the function cannot connect to the specified machine or a docking station is not present.


### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, the function returns one of the CR_-prefixed error codes that are defined in <i>Cfgmgr32.h</i>.




## -remarks



Use this function to determine whether a docking station is present in a local or a remote machine. You can also use the following related functions with docking stations:

<ul>
<li>

<a href="https://msdn.microsoft.com/1c07dca9-5209-46d5-a0a3-87a615e3d40a">CM_Is_Dock_Station_Present</a> identifies whether a docking station is present in a local machine.

</li>
<li>

<a href="https://msdn.microsoft.com/45d8151a-67d0-4cb1-8593-4cfb271a3411">CM_Request_Eject_PC</a> requests that a portable PC, which is inserted in a local docking station, be ejected.

</li>
<li>

<a href="https://msdn.microsoft.com/69bcbfa4-fb89-4b5f-bd0a-260569dfb466">CM_Request_Eject_PC_Ex</a> requests that a portable PC, which is inserted in a local or a remote docking station, be ejected.

</li>
</ul>
 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/1c07dca9-5209-46d5-a0a3-87a615e3d40a">CM_Is_Dock_Station_Present</a>



<a href="https://msdn.microsoft.com/45d8151a-67d0-4cb1-8593-4cfb271a3411">CM_Request_Eject_PC</a>



<a href="https://msdn.microsoft.com/69bcbfa4-fb89-4b5f-bd0a-260569dfb466">CM_Request_Eject_PC_Ex</a>
 

 

