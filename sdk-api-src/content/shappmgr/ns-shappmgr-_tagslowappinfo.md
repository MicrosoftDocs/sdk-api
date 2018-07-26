---
UID: NS:shappmgr._tagSlowAppInfo
title: "_tagSlowAppInfo"
author: windows-sdk-content
description: Provides specialized application information to Add/Remove Programs in Control Panel. This structure is not applicable to published applications.
old-location: shell\SLOWAPPINFO.htm
old-project: shell
ms.assetid: e9af8c70-0f03-4f16-bbfb-5e54f7c6c9df
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: "*PSLOWAPPINFO, SLOWAPPINFO, SLOWAPPINFO structure [Windows Shell], _tagSlowAppInfo, inet_SLOWAPPINFO, shappmgr/SLOWAPPINFO, shell.SLOWAPPINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SLOWAPPINFO, *PSLOWAPPINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shappmgr.h
api_name:
 - SLOWAPPINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _tagSlowAppInfo structure


## -description


Provides specialized application information to <b>Add/Remove Programs</b> in Control Panel. This structure is not applicable to published applications.


## -struct-fields




### -field ullSize

Type: <b>ULONGLONG</b>

The size of the application in bytes.


### -field ftLastUsed

Type: <b>FILETIME</b>

The time the application was last used.


### -field iTimesUsed

Type: <b>int</b>

The count of times the application has been used.


### -field pszImage

Type: <b>LPWSTR</b>

A pointer to a string containing the path to the image that represents the application. The string buffer must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/02f8e527-1c3c-4a2e-bf55-4f33c6a7b822">IShellApp::GetSlowAppInfo</a> and <a href="https://msdn.microsoft.com/655edc51-0967-4b94-9eef-da213e735e0a">IShellApp::GetCachedSlowAppInfo</a> interfaces, neither of which are applicable to published applications. Therefore, this structure is also not applicable to published applications.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>
 

 

