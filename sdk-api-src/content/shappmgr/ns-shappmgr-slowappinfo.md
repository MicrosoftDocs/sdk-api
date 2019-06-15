---
UID: NS:shappmgr._tagSlowAppInfo
title: SLOWAPPINFO (shappmgr.h)
author: windows-sdk-content
description: Provides specialized application information to Add/Remove Programs in Control Panel. This structure is not applicable to published applications.
old-location: shell\SLOWAPPINFO.htm
tech.root: shell
ms.assetid: e9af8c70-0f03-4f16-bbfb-5e54f7c6c9df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSLOWAPPINFO, SLOWAPPINFO, SLOWAPPINFO structure [Windows Shell], inet_SLOWAPPINFO, shappmgr/SLOWAPPINFO, shell.SLOWAPPINFO"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: SLOWAPPINFO, *PSLOWAPPINFO
req.redist: 
ms.custom: 19H1
---

# SLOWAPPINFO structure


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

A pointer to a string containing the path to the image that represents the application. The string buffer must be allocated using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -remarks



This structure is used by the <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getslowappinfo">IShellApp::GetSlowAppInfo</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ishellapp-getcachedslowappinfo">IShellApp::GetCachedSlowAppInfo</a> interfaces, neither of which are applicable to published applications. Therefore, this structure is also not applicable to published applications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>
 

 

