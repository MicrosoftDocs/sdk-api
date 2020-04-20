---
UID: NF:wuapi.IUpdateHistoryEntry.get_Description
title: IUpdateHistoryEntry::get_Description (wuapi.h)
description: Gets the description of an update.helpviewer_keywords: ["Description property [Windows Update Agent]","Description property [Windows Update Agent]","IUpdateHistoryEntry interface","IUpdateHistoryEntry interface [Windows Update Agent]","Description property","IUpdateHistoryEntry.Description","IUpdateHistoryEntry.get_Description","IUpdateHistoryEntry::Description","IUpdateHistoryEntry::get_Description","get_Description","wua.iupdatehistoryentry_description","wuapi/IUpdateHistoryEntry::Description","wuapi/IUpdateHistoryEntry::get_Description"]
old-location: wua\iupdatehistoryentry_description.htm
tech.root: Wua_Sdk
ms.assetid: 355d4623-a84e-4994-ad41-cb4237feeaab
ms.date: 12/05/2018
ms.keywords: Description property [Windows Update Agent], Description property [Windows Update Agent],IUpdateHistoryEntry interface, IUpdateHistoryEntry interface [Windows Update Agent],Description property, IUpdateHistoryEntry.Description, IUpdateHistoryEntry.get_Description, IUpdateHistoryEntry::Description, IUpdateHistoryEntry::get_Description, get_Description, wua.iupdatehistoryentry_description, wuapi/IUpdateHistoryEntry::Description, wuapi/IUpdateHistoryEntry::get_Description
f1_keywords:
- wuapi/IUpdateHistoryEntry.Description
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IUpdateHistoryEntry.Description
- IUpdateHistoryEntry.get_Description
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateHistoryEntry::get_Description


## -description


Gets the description of an update.

This property is read-only.


## -parameters


## -remarks



The information that   this property returns is for the default user interface (UI) language of the user. However, note the following: 

<ul>
<li>If the default UI language of the user is unavailable, Windows Update Agent (WUA) uses the default UI language of the computer.</li>
<li>If the default language of the computer is unavailable, WUA uses the language that the provider of the  update recommends.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid">IUpdateHistoryEntry.ClientApplicationID</a>
 

 

