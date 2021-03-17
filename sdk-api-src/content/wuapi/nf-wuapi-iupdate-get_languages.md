---
UID: NF:wuapi.IUpdate.get_Languages
title: IUpdate::get_Languages (wuapi.h)
description: Gets an interface that contains the languages that are supported by the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","Languages property","IUpdate.Languages","IUpdate.get_Languages","IUpdate::Languages","IUpdate::get_Languages","Languages property [Windows Update Agent]","Languages property [Windows Update Agent]","IUpdate interface","get_Languages","wua.iupdate_language","wuapi/IUpdate::Languages","wuapi/IUpdate::get_Languages"]
old-location: wua\iupdate_language.htm
tech.root: wua
ms.assetid: 788942cc-5cfa-4ce3-bcf6-05c78a817ec8
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],Languages property, IUpdate.Languages, IUpdate.get_Languages, IUpdate::Languages, IUpdate::get_Languages, Languages property [Windows Update Agent], Languages property [Windows Update Agent],IUpdate interface, get_Languages, wua.iupdate_language, wuapi/IUpdate::Languages, wuapi/IUpdate::get_Languages
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
 - IUpdate::get_Languages
 - wuapi/IUpdate::get_Languages
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
 - IUpdate.Languages
 - IUpdate.get_Languages
---

# IUpdate::get_Languages


## -description

Gets an interface that contains the languages that are supported by the update.

This property is read-only.

## -parameters

## -remarks

This property refers to the language of the update itself.  The language that is used for the title and description of the update is not necessarily the language of the update itself.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>