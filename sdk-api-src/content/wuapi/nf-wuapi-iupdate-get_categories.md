---
UID: NF:wuapi.IUpdate.get_Categories
title: IUpdate::get_Categories (wuapi.h)
description: Gets an interface that contains a collection of categories to which the update belongs.
helpviewer_keywords: ["Categories property [Windows Update Agent]","Categories property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","Categories property","IUpdate.Categories","IUpdate.get_Categories","IUpdate::Categories","IUpdate::get_Categories","get_Categories","wua.iupdate_categories","wuapi/IUpdate::Categories","wuapi/IUpdate::get_Categories"]
old-location: wua\iupdate_categories.htm
tech.root: wua
ms.assetid: 25620fc2-25f2-4626-9e41-b44c305c505c
ms.date: 12/05/2018
ms.keywords: Categories property [Windows Update Agent], Categories property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],Categories property, IUpdate.Categories, IUpdate.get_Categories, IUpdate::Categories, IUpdate::get_Categories, get_Categories, wua.iupdate_categories, wuapi/IUpdate::Categories, wuapi/IUpdate::get_Categories
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
 - IUpdate::get_Categories
 - wuapi/IUpdate::get_Categories
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
 - IUpdate.Categories
 - IUpdate.get_Categories
---

# IUpdate::get_Categories


## -description

Gets an interface that contains a  collection of categories to which the update belongs.

This property is read-only.

## -parameters

## -remarks

If the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is  created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that  this property returns is for the language that is specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that was used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>, or if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface is  not  created by using <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a>, the information  that   this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.

Because there is a <b>Categories</b> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> and a <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry2-get_categories">Categories</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a>, the information that is used by the localized properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface depend on the WUA object that owns the <b>ICategory</b> interface. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdate</b>, it follows the localization rules of <b>IUpdate</b>. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdateHistoryEntry2</b>, it follows the localization rules of <b>IUpdateHistoryEntry2</b>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>