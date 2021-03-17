---
UID: NS:appmgmt._APPCATEGORYINFO
title: APPCATEGORYINFO (appmgmt.h)
description: Provides application category information to Add/Remove Programs in Control Panel. The APPCATEGORYINFOLIST structure is used create a complete list of categories for an application publisher.
helpviewer_keywords: ["APPCATEGORYINFO","APPCATEGORYINFO structure [Windows Shell]","_APPCATEGORYINFO","appmgmt/APPCATEGORYINFO","inet_APPCATEGORYINFO","shell.APPCATEGORYINFO"]
old-location: shell\APPCATEGORYINFO.htm
tech.root: shell
ms.assetid: 7a0e61cb-97f8-4ca2-a85a-889e671099d0
ms.date: 12/05/2018
ms.keywords: APPCATEGORYINFO, APPCATEGORYINFO structure [Windows Shell], _APPCATEGORYINFO, appmgmt/APPCATEGORYINFO, inet_APPCATEGORYINFO, shell.APPCATEGORYINFO
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
targetos: Windows
req.typenames: APPCATEGORYINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _APPCATEGORYINFO
 - appmgmt/_APPCATEGORYINFO
 - APPCATEGORYINFO
 - appmgmt/APPCATEGORYINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Appmgmt.h
api_name:
 - APPCATEGORYINFO
---

# APPCATEGORYINFO structure


## -description

Provides application category information to Add/Remove Programs in Control Panel. The <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a> structure is used create a complete list of categories for an application publisher.

## -struct-fields

### -field Locale

Type: <b>LCID</b>

Unused.

### -field pszDescription

Type: <b>LPWSTR</b>

A pointer to a string containing the display name of the category. This string displays in the <b>Category</b> list in Add/Remove Programs. This string buffer must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field AppCategoryId

Type: <b>GUID</b>

A GUID identifying the application category.

## -see-also

<a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a>



<a href="/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-getcategories">IAppPublisher::GetCategories</a>