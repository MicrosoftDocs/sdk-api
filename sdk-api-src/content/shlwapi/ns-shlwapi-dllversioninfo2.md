---
UID: NS:shlwapi._DLLVERSIONINFO2
title: DLLVERSIONINFO2 (shlwapi.h)
author: windows-sdk-content
description: Receives DLL-specific version information. It is used with the DllGetVersion function.
old-location: shell\DLLVERSIONINFO2_0rjh.htm
tech.root: shell
ms.assetid: 1648924d-0727-4cee-80d3-f97550f235cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DLLVERSIONINFO2, DLLVERSIONINFO2 structure [Windows Shell], _win32_DLLVERSIONINFO2_0rjh, shell.DLLVERSIONINFO2_0rjh, shlwapi/DLLVERSIONINFO2
ms.topic: struct
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - DLLVERSIONINFO2
product: Windows
targetos: Windows
req.typenames: DLLVERSIONINFO2
req.redist: 
---

# DLLVERSIONINFO2 structure


## -description


Receives DLL-specific version information. It is used with the <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a> function.


## -struct-fields




### -field info1

Type: <b><a href="https://msdn.microsoft.com/bc6d856c-027f-43df-9bbc-a76f560dddb0">DLLVERSIONINFO</a></b>

A <a href="https://msdn.microsoft.com/bc6d856c-027f-43df-9bbc-a76f560dddb0">DLLVERSIONINFO</a> structure. This member is included to provide backward compatibility with applications that are not expecting a <b>DLLVERSIONINFO2</b> structure.


### -field dwFlags

Type: <b>DWORD</b>

Reserved.


### -field ullVersion

Type: <b>ULONGLONG</b>

A value that contains the version information. It is divided into four 16-bitfields containing the major and minor version numbers, the build number, and the hotfix version, in that order. Use the <a href="https://msdn.microsoft.com/10c75c91-9642-4877-845e-8c6343721b4f">MAKEDLLVERULL</a> macro to construct this value.


## -remarks



Your application must set the <b>cbSize</b> member of the structure pointed to by <b>info1</b> to <b>sizeof(</b><b>DLLVERSIONINFO2</b><b>)</b> before calling <a href="https://msdn.microsoft.com/d7ec0f7d-ba2f-4aa4-b867-a2615244a580">DllGetVersion</a>. Otherwise, no value will be assigned to the <b>dwFlags</b> or <b>ullVersion</b> member of the <b>DLLVERSIONINFO2</b> structure.



