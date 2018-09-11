---
UID: NS:appmgmt._APPCATEGORYINFO
title: "_APPCATEGORYINFO"
author: windows-sdk-content
description: Provides application category information to Add/Remove Programs in Control Panel. The APPCATEGORYINFOLIST structure is used create a complete list of categories for an application publisher.
old-location: shell\APPCATEGORYINFO.htm
tech.root: shell
ms.assetid: 7a0e61cb-97f8-4ca2-a85a-889e671099d0
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: APPCATEGORYINFO, APPCATEGORYINFO structure [Windows Shell], _APPCATEGORYINFO, appmgmt/APPCATEGORYINFO, inet_APPCATEGORYINFO, shell.APPCATEGORYINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: appmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
 - Appmgmt.h
api_name:
 - APPCATEGORYINFO
product: Windows
targetos: Windows
req.typenames: APPCATEGORYINFO
req.redist: 
---

# _APPCATEGORYINFO structure


## -description


Provides application category information to Add/Remove Programs in Control Panel. The <a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a> structure is used create a complete list of categories for an application publisher.


## -struct-fields




### -field Locale

Type: <b>LCID</b>

Unused.


### -field pszDescription

Type: <b>LPWSTR</b>

A pointer to a string containing the display name of the category. This string displays in the <b>Category</b> list in Add/Remove Programs. This string buffer must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field AppCategoryId

Type: <b>GUID</b>

A GUID identifying the application category.


## -see-also




<a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a>



<a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>
 

 

