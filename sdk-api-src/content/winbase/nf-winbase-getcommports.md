---
UID: NF:winbase.GetCommPorts
title: GetCommPorts function
author: windows-sdk-content
description: Gets an array that contains the well-formed COM ports.
old-location: base\getcommports.htm
old-project: DevIO
ms.assetid: 8E57FB62-D7A0-4B47-942B-E33E0B7A37B1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCommPorts, GetCommPorts function, base.getcommports, winbase/GetCommPorts
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps | UWP apps]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommPorts
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCommPorts function


## -description


Gets an array that contains the well-formed COM ports.

This function obtains the COM port numbers from the <b>HKLM\Hardware\DeviceMap\SERIALCOMM</b> registry key and then writes them to a caller-supplied array. If the array is too small, the function gets the necessary size. 
<div class="alert"><b>Note</b>  If new entries are added to the registry key, the necessary size can changes between API calls.</div><div> </div>

## -parameters




### -param lpPortNumbers [out]

An array for the port numbers.


### -param uPortNumbersCount [in]

The length of the array in the <i>lpPortNumbers</i> parameter.


### -param puPortNumbersFound [out]

The number of port numbers written to the <i>lpPortNumbers</i> or the length of the array required for the port numbers.


## -returns







