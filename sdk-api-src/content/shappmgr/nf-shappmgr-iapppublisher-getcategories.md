---
UID: NF:shappmgr.IAppPublisher.GetCategories
title: IAppPublisher::GetCategories (shappmgr.h)
description: Retrieves a structure listing the categories provided by an application publisher.
helpviewer_keywords: ["GetCategories","GetCategories method [Windows Shell]","GetCategories method [Windows Shell]","IAppPublisher interface","IAppPublisher interface [Windows Shell]","GetCategories method","IAppPublisher.GetCategories","IAppPublisher::GetCategories","inet_IAppPublisher_GetCategories","shappmgr/IAppPublisher::GetCategories","shell.IAppPublisher_GetCategories"]
old-location: shell\IAppPublisher_GetCategories.htm
tech.root: shell
ms.assetid: 139a5094-8bb3-4b5d-938d-ba4af5d52d94
ms.date: 12/05/2018
ms.keywords: GetCategories, GetCategories method [Windows Shell], GetCategories method [Windows Shell],IAppPublisher interface, IAppPublisher interface [Windows Shell],GetCategories method, IAppPublisher.GetCategories, IAppPublisher::GetCategories, inet_IAppPublisher_GetCategories, shappmgr/IAppPublisher::GetCategories, shell.IAppPublisher_GetCategories
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppPublisher::GetCategories
 - shappmgr/IAppPublisher::GetCategories
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IAppPublisher.GetCategories
---

# IAppPublisher::GetCategories


## -description

Retrieves a structure listing the categories provided by an application publisher.

## -parameters

### -param pAppCategoryList [out]

Type: <b><a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a>*</b>

A pointer to an <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a> structure. This structure's <b>cCategory</b> member returns the count of supported categories. The <b>pCategoryInfo</b> member returns a pointer to an array of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a> structures. This array contains all the categories an application publisher supports and must be allocated using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Add/Remove Programs Control Panel Application passes the ID returned for a category to the <a href="/windows/desktop/api/shappmgr/nf-shappmgr-iapppublisher-enumapps">IAppPublisher::EnumApps</a> method to identify which category is to be enumerated.


#### Examples

The following example shows how to calculate the size of the array of <a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a> structures that is returned by <b>IAppPublisher::GetCategories</b>.


```cpp
size_t CategoryListArraySize = sizeof(APPCATEGORYINFO) * pInfoList->cCategory;
```

## -see-also

<a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfo">APPCATEGORYINFO</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-appcategoryinfolist">APPCATEGORYINFOLIST</a>



<a href="/windows/desktop/api/shappmgr/nn-shappmgr-iapppublisher">IAppPublisher</a>