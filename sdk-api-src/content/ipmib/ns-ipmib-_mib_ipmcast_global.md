---
UID: NS:ipmib._MIB_IPMCAST_GLOBAL
title: "_MIB_IPMCAST_GLOBAL"
author: windows-sdk-content
description: Stores global information for IP multicast on a particular computer.
old-location: mib\mib_ipmcast_global.htm
old-project: MIB
ms.assetid: b967a064-0c89-47eb-8c7c-eb1b9141e5d7
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_IPMCAST_GLOBAL, MIB_IPMCAST_GLOBAL, MIB_IPMCAST_GLOBAL structure [MIB], PMIB_IPMCAST_GLOBAL, PMIB_IPMCAST_GLOBAL structure pointer [MIB], _MIB_IPMCAST_GLOBAL, _mpr_mib_ipmcast_global, ipmib/MIB_IPMCAST_GLOBAL, ipmib/PMIB_IPMCAST_GLOBAL, iprtrmib/MIB_IPMCAST_GLOBAL, iprtrmib/PMIB_IPMCAST_GLOBAL, mib.mib_ipmcast_global, rras.mib_ipmcast_global"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MIB_IPMCAST_GLOBAL, *PMIB_IPMCAST_GLOBAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPMCAST_GLOBAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MIB_IPMCAST_GLOBAL structure


## -description


The 
<b>MIB_IPMCAST_GLOBAL</b> structure stores global information for IP multicast on a particular computer.


## -struct-fields




### -field dwEnable

Specifies whether IP multicast is enabled on the computer.


## -remarks



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista
   and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/59bc8df1-3999-4acb-b556-e765a9faef79">MIB_IPMCAST_IF_ENTRY</a>



<a href="https://msdn.microsoft.com/731e2c88-5c4f-4165-a9f2-287b4c10c76b">MIB_IPMCAST_MFE</a>



<a href="https://msdn.microsoft.com/4ad35cc0-50e2-47b9-8ce3-9bf8e7032c40">MIB_IPMCAST_OIF</a>
 

 

