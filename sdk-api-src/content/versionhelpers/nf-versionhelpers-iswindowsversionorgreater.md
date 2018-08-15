---
UID: NF:versionhelpers.IsWindowsVersionOrGreater
title: IsWindowsVersionOrGreater function
author: windows-sdk-content
description: Indicates if the current OS version matches, or is greater than, the provided version information.
old-location: base\iswindowsversionorgreater.htm
old-project: SysInfo
ms.assetid: B28DFEC0-A94E-49F6-9DF0-4EE470EC4AF5
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IsWindowsVersionOrGreater, IsWindowsVersionOrGreater function, base.iswindowsversionorgreater, versionhelpers/IsWindowsVersionOrGreater
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: versionhelpers.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VersionHelpers.h
api_name:
 - IsWindowsVersionOrGreater
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

