---
UID: NF:cfgmgr32.CM_Get_Version_Ex
title: CM_Get_Version_Ex function
author: windows-sdk-content
description: The CM_Get_Version_Ex function returns version 4.0 of the Plug and Play (PnP) Configuration Manager DLL (Cfgmgr32.dll) for a local or a remote machine.
old-location: devinst\cm_get_version_ex.htm
tech.root: devinst
ms.assetid: f189a417-48a4-436e-bb1c-6b0c9f066c04
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CM_Get_Version_Ex, CM_Get_Version_Ex function [Device and Driver Installation], cfgmgr32/CM_Get_Version_Ex, cfgmgrfn_0c27aa6b-5682-4901-b57b-2477a0cb9919.xml, devinst.cm_get_version_ex
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
 - CM_Get_Version_Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_Version_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Get_Version_Ex</b> function returns version 4.0 of the Plug and Play (PnP) Configuration Manager <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DLL</a> (<i>Cfgmgr32.dll</i>) for a local or a remote machine. 


## -parameters




### -param hMachine [in, optional]

Supplies a machine handle that is returned by <a href="https://msdn.microsoft.com/4108a35f-0861-4142-a798-731287515910">CM_Connect_Machine</a>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the function succeeds, it returns the major revision number in the high-order byte and the minor revision number in the low-order byte. Version 4.0 is returned as 0x0400. By default, version 4.0 is supported  by Microsoft Windows 2000 and later versions of Windows. If an internal error occurs, the function returns 0x0000. Call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> to obtain the error code for the failure.




## -remarks



This function returns version 4.0 of the configuration manager to ensure compatibility with version 4.0 and all later versions of the configuration manager, and to ensure compatibility with all applications that require version 4.0 of the configuration manager.

To determine if a specific version of the configuration manager is available on a machine, use <a href="https://msdn.microsoft.com/a7a1e8d0-7645-423a-8123-a58ed7ae9827">CM_Is_Version_Available</a> or <a href="https://msdn.microsoft.com/a6728f01-7899-46e3-8cda-19a5c46f4992">CM_Is_Version_Available_Ex</a>.

 Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/998c6c57-b242-4aa0-8c9f-cfff61d2a642">CM_Get_Version</a>



<a href="https://msdn.microsoft.com/a7a1e8d0-7645-423a-8123-a58ed7ae9827">CM_Is_Version_Available</a>



<a href="https://msdn.microsoft.com/a6728f01-7899-46e3-8cda-19a5c46f4992">CM_Is_Version_Available_Ex</a>
 

 

