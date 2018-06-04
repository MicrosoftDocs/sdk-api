---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# CM_Get_Version_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Get_Version_Ex</b> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DLL</a> (<i>Cfgmgr32.dll</i>) for a local or a remote machine. 


## -parameters




### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff537948">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the function succeeds, it returns the major revision number in the high-order byte and the minor revision number in the low-order byte. Version 4.0 is returned as 0x0400. By default, version 4.0 is supported  by Microsoft Windows 2000 and later versions of Windows. If an internal error occurs, the function returns 0x0000. Call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> to obtain the error code for the failure.




## -remarks



This function returns version 4.0 of the configuration manager to ensure compatibility with version 4.0 and all later versions of the configuration manager, and to ensure compatibility with all applications that require version 4.0 of the configuration manager.

To determine if a specific version of the configuration manager is available on a machine, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538736">CM_Is_Version_Available</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538739">CM_Is_Version_Available_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538686">CM_Get_Version</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538736">CM_Is_Version_Available</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538739">CM_Is_Version_Available_Ex</a>
 

 

