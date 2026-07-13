---
UID: NF:wuapi.IUpdateSession2.get_UserLocale
title: IUpdateSession2::get_UserLocale (wuapi.h)
description: Gets and sets the preferred locale for which update information is retrieved.. (Get)
helpviewer_keywords: ["IUpdateSession2 interface [Windows Update Agent]","UserLocale property","IUpdateSession2.UserLocale","IUpdateSession2.get_UserLocale","IUpdateSession2::UserLocale","IUpdateSession2::get_UserLocale","IUpdateSession2::put_UserLocale","UserLocale property [Windows Update Agent]","UserLocale property [Windows Update Agent]","IUpdateSession2 interface","get_UserLocale","wua.iupdatesession2_userlocale","wuapi/IUpdateSession2::UserLocale","wuapi/IUpdateSession2::get_UserLocale","wuapi/IUpdateSession2::put_UserLocale"]
old-location: wua\iupdatesession2_userlocale.htm
tech.root: wua
ms.assetid: 30ee1836-ea70-4dd1-b531-a7ca32ca940d
ms.date: 12/05/2018
ms.keywords: IUpdateSession2 interface [Windows Update Agent],UserLocale property, IUpdateSession2.UserLocale, IUpdateSession2.get_UserLocale, IUpdateSession2::UserLocale, IUpdateSession2::get_UserLocale, IUpdateSession2::put_UserLocale, UserLocale property [Windows Update Agent], UserLocale property [Windows Update Agent],IUpdateSession2 interface, get_UserLocale, wua.iupdatesession2_userlocale, wuapi/IUpdateSession2::UserLocale, wuapi/IUpdateSession2::get_UserLocale, wuapi/IUpdateSession2::put_UserLocale
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
 - IUpdateSession2::get_UserLocale
 - wuapi/IUpdateSession2::get_UserLocale
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
 - IUpdateSession2.UserLocale
 - IUpdateSession2.get_UserLocale
 - IUpdateSession2.put_UserLocale
---

# IUpdateSession2::get_UserLocale


## -description

Gets and sets the preferred locale for which update information is retrieved.. 

If you do not specify the locale, the default is the user locale that   <a href="/windows/desktop/api/winnls/nf-winnls-getuserdefaultuilanguage">GetUserDefaultUILanguage</a> returns. If the information is not available in a specified locale or in the user locale, Windows Update Agent (WUA) tries to retrieve the information from the default update locale.

This property is read/write.

## -parameters

## -remarks

A search from an <b>UpdateSearch</b> object that was created from the <b>UpdateSession</b> object fails if the following conditions are true:

<ul>
<li>A user or a power user set the <b>UserLocale</b> property for the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface to a locale.</li>
<li>The locale corresponds to a language that is not installed on the computer.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>
