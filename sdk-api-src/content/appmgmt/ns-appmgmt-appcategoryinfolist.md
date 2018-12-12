---
UID: NS:appmgmt._APPCATEGORYINFOLIST
title: APPCATEGORYINFOLIST
author: windows-sdk-content
description: Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.
old-location: shell\APPCATEGORYINFOLIST.htm
tech.root: shell
ms.assetid: c590d9ab-ab41-4192-a6c2-c6c2c931e873
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: APPCATEGORYINFOLIST, APPCATEGORYINFOLIST structure [Windows Shell], _APPCATEGORYINFOLIST, appmgmt/APPCATEGORYINFOLIST, inet_APPCATEGORYINFOLIST, shell.APPCATEGORYINFOLIST
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - APPCATEGORYINFOLIST
product: Windows
targetos: Windows
req.typenames: APPCATEGORYINFOLIST
req.redist: 
---

# APPCATEGORYINFOLIST structure


## -description


Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.  


## -struct-fields




### -field cCategory

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the count of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> elements in the array pointed to by <b>pCategoryInfo</b>.


### -field pCategoryInfo

Type: <b><a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a>*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> structures. This array contains all the categories an application publisher supports and must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
        


### -field pCategoryInfo.size_is

 


### -field pCategoryInfo.size_is.cCategory

 




## -see-also




<a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a>



<a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>
 

 

