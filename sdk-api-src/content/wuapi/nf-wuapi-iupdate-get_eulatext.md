---
UID: NF:wuapi.IUpdate.get_EulaText
title: IUpdate::get_EulaText (wuapi.h)
description: Gets the full localized text of the Microsoft Software License Terms that are associated with the update.
helpviewer_keywords: ["EulaText property [Windows Update Agent]","EulaText property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","EulaText property","IUpdate.EulaText","IUpdate.get_EulaText","IUpdate::EulaText","IUpdate::get_EulaText","get_EulaText","wua.iupdate_eulatext","wuapi/IUpdate::EulaText","wuapi/IUpdate::get_EulaText"]
old-location: wua\iupdate_eulatext.htm
tech.root: wua
ms.assetid: 4c3ddc9c-0261-46e8-92df-d125fea46991
ms.date: 12/05/2018
ms.keywords: EulaText property [Windows Update Agent], EulaText property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],EulaText property, IUpdate.EulaText, IUpdate.get_EulaText, IUpdate::EulaText, IUpdate::get_EulaText, get_EulaText, wua.iupdate_eulatext, wuapi/IUpdate::EulaText, wuapi/IUpdate::get_EulaText
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
 - IUpdate::get_EulaText
 - wuapi/IUpdate::get_EulaText
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
 - IUpdate.EulaText
 - IUpdate.get_EulaText
---

# IUpdate::get_EulaText


## -description

Gets the full localized text of the Microsoft Software License Terms that are associated with the update.

This property is read-only.

## -parameters

## -remarks

If the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is  created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is  specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property. This is the <b>UserLocale</b> property  of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>, or if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is not  created by using <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a>, the information that is returned by  this property is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>