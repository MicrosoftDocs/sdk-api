---
UID: NF:iphlpapi.GetNumberOfInterfaces
title: GetNumberOfInterfaces function
author: windows-sdk-content
description: The GetNumberOfInterfaces functions retrieves the number of interfaces on the local computer.
old-location: iphlp\getnumberofinterfaces.htm
tech.root: IpHlp
ms.assetid: 655d63eb-455a-4a5e-97e2-7b7588eee4d9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNumberOfInterfaces, GetNumberOfInterfaces function [IP Helper], _iphlp_getnumberofinterfaces, iphlp.getnumberofinterfaces, iphlpapi/GetNumberOfInterfaces
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetNumberOfInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumberOfInterfaces function


## -description


The 
<b>GetNumberOfInterfaces</b> functions retrieves the number of interfaces on the local computer.


## -parameters




### -param pdwNumIf [out]

Pointer to a <b>DWORD</b> variable that receives the number of interfaces on the local computer.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -remarks



The 
<b>GetNumberOfInterfaces</b> function returns the number of interfaces on the local computer, including the loopback interface. This number is one more than the number of adapters returned by the 
<a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a> and 
<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a> functions because these functions do not return information about the loopback interface.




## -see-also




<a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a>



<a href="https://msdn.microsoft.com/bf16588d-3756-469e-afa2-e2e3dd537047">GetIfEntry</a>



<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>
 

 

