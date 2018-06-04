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

# _DLLVERSIONINFO2 structure


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



