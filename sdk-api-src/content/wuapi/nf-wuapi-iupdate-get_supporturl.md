---
UID: NF:wuapi.IUpdate.get_SupportUrl
title: IUpdate::get_SupportUrl (wuapi.h)
description: Gets a hyperlink to the language-specific support information for the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","SupportUrl property","IUpdate.SupportUrl","IUpdate.get_SupportUrl","IUpdate::SupportUrl","IUpdate::get_SupportUrl","SupportUrl property [Windows Update Agent]","SupportUrl property [Windows Update Agent]","IUpdate interface","get_SupportUrl","wua.iupdate_supporturl","wuapi/IUpdate::SupportUrl","wuapi/IUpdate::get_SupportUrl"]
old-location: wua\iupdate_supporturl.htm
tech.root: wua
ms.assetid: c4734e71-a64d-4231-80ed-1ee2bcc98ce1
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],SupportUrl property, IUpdate.SupportUrl, IUpdate.get_SupportUrl, IUpdate::SupportUrl, IUpdate::get_SupportUrl, SupportUrl property [Windows Update Agent], SupportUrl property [Windows Update Agent],IUpdate interface, get_SupportUrl, wua.iupdate_supporturl, wuapi/IUpdate::SupportUrl, wuapi/IUpdate::get_SupportUrl
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
 - IUpdate::get_SupportUrl
 - wuapi/IUpdate::get_SupportUrl
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
 - IUpdate.SupportUrl
 - IUpdate.get_SupportUrl
---

# IUpdate::get_SupportUrl


## -description

Gets a hyperlink to the language-specific support information for the update.

This property is read-only.

## -parameters

## -remarks

If the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is  created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is  specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property. This is the <b>UserLocale</b> property  of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>, or if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is not  created by using <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a>, the information that is returned by  this property is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>