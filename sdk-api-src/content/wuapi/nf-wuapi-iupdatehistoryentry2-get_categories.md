---
UID: NF:wuapi.IUpdateHistoryEntry2.get_Categories
title: IUpdateHistoryEntry2::get_Categories (wuapi.h)
description: Gets a collection of the update categories to which an update belongs.
helpviewer_keywords: ["Categories property [Windows Update Agent]","Categories property [Windows Update Agent]","IUpdateHistoryEntry2 interface","IUpdateHistoryEntry2 interface [Windows Update Agent]","Categories property","IUpdateHistoryEntry2.Categories","IUpdateHistoryEntry2.get_Categories","IUpdateHistoryEntry2::Categories","IUpdateHistoryEntry2::get_Categories","get_Categories","wua.iupdatehistoryentry2_categories","wuapi/IUpdateHistoryEntry2::Categories","wuapi/IUpdateHistoryEntry2::get_Categories"]
old-location: wua\iupdatehistoryentry2_categories.htm
tech.root: wua
ms.assetid: b821d608-61c2-4442-8b7e-18e27006602b
ms.date: 12/05/2018
ms.keywords: Categories property [Windows Update Agent], Categories property [Windows Update Agent],IUpdateHistoryEntry2 interface, IUpdateHistoryEntry2 interface [Windows Update Agent],Categories property, IUpdateHistoryEntry2.Categories, IUpdateHistoryEntry2.get_Categories, IUpdateHistoryEntry2::Categories, IUpdateHistoryEntry2::get_Categories, get_Categories, wua.iupdatehistoryentry2_categories, wuapi/IUpdateHistoryEntry2::Categories, wuapi/IUpdateHistoryEntry2::get_Categories
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
 - IUpdateHistoryEntry2::get_Categories
 - wuapi/IUpdateHistoryEntry2::get_Categories
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
 - IUpdateHistoryEntry2.Categories
 - IUpdateHistoryEntry2.get_Categories
---

# IUpdateHistoryEntry2::get_Categories


## -description

Gets a collection of the update categories to which an update belongs.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface  may require you to update Windows Update Agent (WUA). For more information, see <a href="/windows/desktop/Wua_Sdk/updating-the-windows-update-agent">Updating Windows Update Agent</a>.

The information that this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language that  the provider of the  update recommends.

Because there is a <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface and a <b>Categories</b> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a> interface, the information that is used by the localized properties of the <a href="/windows/desktop/api/wuapi/nn-wuapi-icategory">ICategory</a> interface depends on the WUA object that owns the <b>ICategory</b> interface. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdate</b>, it follows the localization rules of <b>IUpdate</b>. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdateHistoryEntry2</b>, it follows the localization rules of <b>IUpdateHistoryEntry2</b>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry2">IUpdateHistoryEntry2</a>