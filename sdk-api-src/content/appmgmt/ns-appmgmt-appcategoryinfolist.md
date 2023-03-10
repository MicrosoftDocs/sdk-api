---
UID: NS:appmgmt._APPCATEGORYINFOLIST
title: APPCATEGORYINFOLIST (appmgmt.h)
description: Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.
helpviewer_keywords: ["APPCATEGORYINFOLIST","APPCATEGORYINFOLIST structure [Windows Shell]","_APPCATEGORYINFOLIST","appmgmt/APPCATEGORYINFOLIST","inet_APPCATEGORYINFOLIST","shell.APPCATEGORYINFOLIST"]
old-location: shell\APPCATEGORYINFOLIST.htm
tech.root: shell
ms.assetid: c590d9ab-ab41-4192-a6c2-c6c2c931e873
ms.date: 12/05/2018
ms.keywords: APPCATEGORYINFOLIST, APPCATEGORYINFOLIST structure [Windows Shell], _APPCATEGORYINFOLIST, appmgmt/APPCATEGORYINFOLIST, inet_APPCATEGORYINFOLIST, shell.APPCATEGORYINFOLIST
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
req.typenames: APPCATEGORYINFOLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _APPCATEGORYINFOLIST
 - appmgmt/_APPCATEGORYINFOLIST
 - APPCATEGORYINFOLIST
 - appmgmt/APPCATEGORYINFOLIST
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
 - APPCATEGORYINFOLIST
---

# APPCATEGORYINFOLIST structure


## -description

Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.

## -struct-fields

### -field cCategory

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the count of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a> elements in the array pointed to by <b>pCategoryInfo</b>.

### -field pCategoryInfo

Type: <b><a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a> structures. This array contains all the categories an application publisher supports and must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field pCategoryInfo.size_is

### -field pCategoryInfo.size_is.cCategory

## -see-also

<a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a>



<a href="/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-getcategories">IAppPublisher::GetCategories</a>