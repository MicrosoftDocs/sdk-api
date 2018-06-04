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

# IsWindowsVersionOrGreater function


## -description


<div class="alert"><b>Important</b>  You should only use this function if the other provided 
   <a href="https://msdn.microsoft.com/2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34">Version Helper functions</a> do not fit within your 
   scenarios.</div><div> </div>Indicates if the current OS version matches, or is greater than, the provided version 
    information. This function is useful in confirming a  version of Windows Server that 
    doesn't share a version number with a client release.


## -parameters




### -param wMajorVersion

The major OS version number.


### -param wMinorVersion

The minor OS version number.


### -param wServicePackMajor

The major Service Pack version number.


## -returns



<b>TRUE</b> if the specified version matches, or is greater than, the version of the 
      current Windows OS; otherwise, <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/5C475B5E-1412-4F60-AB81-00BE83E204BF">IsWindows7OrGreater</a>



<a href="https://msdn.microsoft.com/E8AD3423-91EF-4ECE-9EF2-808C68CEA861">IsWindows7SP1OrGreater</a>



<a href="https://msdn.microsoft.com/D11971C8-2E8F-4AD2-BE0B-FEFEC8949125">IsWindows8OrGreater</a>



<a href="https://msdn.microsoft.com/E391B568-5E43-42C7-B186-8CA524331FFE">IsWindows8Point10OrGreater</a>



<a href="https://msdn.microsoft.com/7CC1DD25-762B-489F-AC20-1B57764923A2">IsWindowsServer</a>



<a href="https://msdn.microsoft.com/556C70DC-6A44-4D85-BDBF-C1110D63DC69">IsWindowsVistaOrGreater</a>



<a href="https://msdn.microsoft.com/7E74A761-E336-4618-B92F-166C3DF1FF66">IsWindowsVistaSP1OrGreater</a>



<a href="https://msdn.microsoft.com/8D7F5DA2-8927-4453-A5E3-35A345B099EC">IsWindowsVistaSP2OrGreater</a>



<a href="https://msdn.microsoft.com/48B7FAD6-569F-4CF5-A413-857679363736">IsWindowsXPOrGreater</a>



<a href="https://msdn.microsoft.com/F8921444-B13D-4522-84F2-4792F4F37EA5">IsWindowsXPSP1OrGreater</a>



<a href="https://msdn.microsoft.com/DA957BA8-AD28-4096-8BE5-B77CA55B9324">IsWindowsXPSP2OrGreater</a>



<a href="https://msdn.microsoft.com/06DC8FF0-8652-4652-855F-600AC53C6301">IsWindowsXPSP3OrGreater</a>
 

 

