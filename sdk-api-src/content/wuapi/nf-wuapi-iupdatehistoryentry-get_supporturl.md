---
UID: NF:wuapi.IUpdateHistoryEntry.get_SupportUrl
title: IUpdateHistoryEntry::get_SupportUrl
author: windows-sdk-content
description: Gets a hyperlink to the language-specific support information for an update.
old-location: wua\iupdatehistoryentry_supporturl.htm
old-project: Wua_Sdk
ms.assetid: 8dabc5db-2741-4399-9cfc-eb79613e0d57
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],SupportUrl property, IUpdateHistoryEntry.SupportUrl, IUpdateHistoryEntry.get_SupportUrl, IUpdateHistoryEntry::SupportUrl, IUpdateHistoryEntry::get_SupportUrl, SupportUrl property [Windows Update Agent], SupportUrl property [Windows Update Agent],IUpdateHistoryEntry interface, get_SupportUrl, wua.iupdatehistoryentry_supporturl, wuapi/IUpdateHistoryEntry::SupportUrl, wuapi/IUpdateHistoryEntry::get_SupportUrl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
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
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>



<a href="https://msdn.microsoft.com/7c2a209f-10e8-4158-8201-a062f86b5fdd">IUpdateHistoryEntry.ClientApplicationID</a>
 

 

