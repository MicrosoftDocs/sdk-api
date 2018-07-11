---
UID: NS:shlwapi._DLLVERSIONINFO
title: "_DLLVERSIONINFO"
author: windows-sdk-content
description: Receives DLL-specific version information.
old-location: shell\DLLVERSIONINFO_0rjh.htm
old-project: shell
ms.assetid: bc6d856c-027f-43df-9bbc-a76f560dddb0
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: DLLVERSIONINFO, DLLVERSIONINFO structure [Windows Shell], DLLVER_PLATFORM_NT, DLLVER_PLATFORM_WINDOWS, _DLLVERSIONINFO, _win32_DLLVERSIONINFO_0rjh, shell.DLLVERSIONINFO_0rjh, shlwapi/DLLVERSIONINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: DLLVERSIONINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - DLLVERSIONINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _DLLVERSIONINFO structure


## -description


Receives DLL-specific version information. It is used with the <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a> function.

            
<div class="alert"><b>Note</b>  In place of this structure, you can use the <a href="https://msdn.microsoft.com/1648924d-0727-4cee-80d3-f97550f235cd">DLLVERSIONINFO2</a> structure.</div><div> </div>

## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. This member must be filled in before calling the function.


### -field dwMajorVersion

Type: <b>DWORD</b>

The major version of the DLL. For instance, if the DLL's version is 4.0.950, this value will be 4.


### -field dwMinorVersion

Type: <b>DWORD</b>

The minor version of the DLL. For instance, if the DLL's version is 4.0.950, this value will be 0.


### -field dwBuildNumber

Type: <b>DWORD</b>

The build number of the DLL. For instance, if the DLL's version is 4.0.950, this value will be 950.


### -field dwPlatformID

Type: <b>DWORD</b>

Identifies the platform for which the DLL was built. This can be one of the following values.



#### DLLVER_PLATFORM_WINDOWS (0x00000001)

The DLL was built for earlier Windows platforms such as Windows 95.



#### DLLVER_PLATFORM_NT (0x00000002)

The DLL was built for platforms such as Windows 2000, Windows Vista, or Windows 7.


## -see-also




<a href="https://msdn.microsoft.com/1648924d-0727-4cee-80d3-f97550f235cd">DLLVERSIONINFO2</a>



<a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a>
 

 

