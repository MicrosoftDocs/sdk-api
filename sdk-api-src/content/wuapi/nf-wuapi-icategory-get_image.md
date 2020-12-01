---
UID: NF:wuapi.ICategory.get_Image
title: ICategory::get_Image (wuapi.h)
description: Gets an interface that contains information about the image that is associated with the category.
helpviewer_keywords: ["ICategory interface [Windows Update Agent]","Image property","ICategory.Image","ICategory.get_Image","ICategory::Image","ICategory::get_Image","Image property [Windows Update Agent]","Image property [Windows Update Agent]","ICategory interface","get_Image","wua.icategory_image","wuapi/ICategory::Image","wuapi/ICategory::get_Image"]
old-location: wua\icategory_image.htm
tech.root: wua
ms.assetid: 41f0dd44-c919-4264-8f35-ea4e48fd5503
ms.date: 12/05/2018
ms.keywords: ICategory interface [Windows Update Agent],Image property, ICategory.Image, ICategory.get_Image, ICategory::Image, ICategory::get_Image, Image property [Windows Update Agent], Image property [Windows Update Agent],ICategory interface, get_Image, wua.icategory_image, wuapi/ICategory::Image, wuapi/ICategory::get_Image
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICategory::get_Image
 - wuapi/ICategory::get_Image
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ICategory.Image
 - ICategory.get_Image
---

# ICategory::get_Image


## -description

Gets an interface that contains information about the image that is associated with the category.

This property is read-only.

## -parameters

## -remarks

A <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a> property exists for the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface. And, a <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry2-get_categories">Categories</a> property exists for the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface. Therefore, the information that is used by the localized properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface depends on the Windows Update Agent (WUA) object that owns the <b>ICategory</b> interface.

 If the <a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface is returned from the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdate</b> interface. In this case, if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface, or if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is not  created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.

If the <a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface is returned from the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry2-get_categories">Categories</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface, the <b>ICategory</b> interface follows the localization rules of the <b>IUpdateHistoryEntry2</b> interface. The information  that   this property returns is for the default UI language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that the provider of the  update recommends.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a>



<a href="/windows/desktop/api/wuapi/nn-wuapi-iimageinformation">IImageInformation</a>