---
UID: NF:wuapi.IUpdate.get_Image
title: IUpdate::get_Image (wuapi.h)
description: Gets an interface that contains information about an image that is associated with the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","Image property","IUpdate.Image","IUpdate.get_Image","IUpdate::Image","IUpdate::get_Image","Image property [Windows Update Agent]","Image property [Windows Update Agent]","IUpdate interface","get_Image","wua.iupdate_image","wuapi/IUpdate::Image","wuapi/IUpdate::get_Image"]
old-location: wua\iupdate_image.htm
tech.root: wua
ms.assetid: 0cae0b5b-8a47-461f-ab91-b9ac80418e20
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],Image property, IUpdate.Image, IUpdate.get_Image, IUpdate::Image, IUpdate::get_Image, Image property [Windows Update Agent], Image property [Windows Update Agent],IUpdate interface, get_Image, wua.iupdate_image, wuapi/IUpdate::Image, wuapi/IUpdate::get_Image
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
 - IUpdate::get_Image
 - wuapi/IUpdate::get_Image
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
 - IUpdate.Image
 - IUpdate.get_Image
---

# IUpdate::get_Image


## -description

Gets an interface that contains information about an image that is associated with the update.

This property is read-only.

## -parameters

## -returns

Returns S_OK if successful. Otherwise, returns a COM or Windows error code.

## -remarks

If the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is  created by using the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a> method, the information  that   this property returns is for the language that is  specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property. This is the <b>UserLocale</b> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a> interface of the session that is used to create <b>IUpdateSearcher</b>.

If a language preference is not specified by the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession2-get_userlocale">UserLocale</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>, or if the <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface  is not  created by using <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">IUpdateSession::CreateUpdateSearcher</a>, the information that is returned by  this property is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language  that  the provider of the  update recommends.

This API can return a null pointer as the output, even when the return value is S_OK.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
