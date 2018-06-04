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

# CM_Is_Version_Available function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated and should not be used.]

The <b>CM_Is_Version_Available</b> function indicates whether a specified version of the Plug and Play (PnP) Configuration Manager <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">DLL</a> (<i>Cfgmgr32.dll</i>) is supported by a local machine.


## -parameters




### -param wVersion [in]

Identifies a version of the configuration manager. The supported version of the configuration manager corresponds directly to the operating system version. The major version is specified by the high-order byte and the minor version is specified by the low-order byte. 

For example, 0x0400 specifies version 4.0, which is supported by default by Microsoft Windows 2000 and later versions of Windows. 0x0501 specifies version 5.1, which is supported by Windows XP and later versions of Windows. 


## -returns



The function returns <b>TRUE</b> if the local machine supports the specified version of the configuration manager. Otherwise, the function returns <b>FALSE</b>.




## -remarks



Use this function to determine whether a specified version of the configuration manager is supported by a local machine. If the specified version is supported, all versions earlier and including this version are supported by the machine. You can also use <a href="https://msdn.microsoft.com/library/windows/hardware/ff538739">CM_Is_Version_Available_Ex</a> to determine if a local or a remote machine supports a specific version of the configuration manager. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538686">CM_Get_Version</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538696">CM_Get_Version_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538739">CM_Is_Version_Available_Ex</a>
 

 

