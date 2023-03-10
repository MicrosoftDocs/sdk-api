---
UID: NF:wuapi.IUpdateHistoryEntry.get_SupportUrl
title: IUpdateHistoryEntry::get_SupportUrl (wuapi.h)
description: Gets a hyperlink to the language-specific support information for an update.
helpviewer_keywords: ["IUpdateHistoryEntry interface [Windows Update Agent]","SupportUrl property","IUpdateHistoryEntry.SupportUrl","IUpdateHistoryEntry.get_SupportUrl","IUpdateHistoryEntry::SupportUrl","IUpdateHistoryEntry::get_SupportUrl","SupportUrl property [Windows Update Agent]","SupportUrl property [Windows Update Agent]","IUpdateHistoryEntry interface","get_SupportUrl","wua.iupdatehistoryentry_supporturl","wuapi/IUpdateHistoryEntry::SupportUrl","wuapi/IUpdateHistoryEntry::get_SupportUrl"]
old-location: wua\iupdatehistoryentry_supporturl.htm
tech.root: wua
ms.assetid: 8dabc5db-2741-4399-9cfc-eb79613e0d57
ms.date: 12/05/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],SupportUrl property, IUpdateHistoryEntry.SupportUrl, IUpdateHistoryEntry.get_SupportUrl, IUpdateHistoryEntry::SupportUrl, IUpdateHistoryEntry::get_SupportUrl, SupportUrl property [Windows Update Agent], SupportUrl property [Windows Update Agent],IUpdateHistoryEntry interface, get_SupportUrl, wua.iupdatehistoryentry_supporturl, wuapi/IUpdateHistoryEntry::SupportUrl, wuapi/IUpdateHistoryEntry::get_SupportUrl
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
 - IUpdateHistoryEntry::get_SupportUrl
 - wuapi/IUpdateHistoryEntry::get_SupportUrl
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
 - IUpdateHistoryEntry.SupportUrl
 - IUpdateHistoryEntry.get_SupportUrl
---

# IUpdateHistoryEntry::get_SupportUrl


## -description

Gets a hyperlink to the language-specific support information for an update.

This property is read-only.

## -parameters

## -remarks

The information that   this property returns is for the default user interface (UI) language of the user. However, note the following: 

<ul>
<li>If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.   </li>
<li>If the default language of the computer is unavailable, WUA uses the language that the provider of the  update recommends.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid">IUpdateHistoryEntry.ClientApplicationID</a>