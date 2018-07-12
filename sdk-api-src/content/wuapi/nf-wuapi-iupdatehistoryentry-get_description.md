---
UID: NF:wuapi.IUpdateHistoryEntry.get_Description
title: IUpdateHistoryEntry::get_Description
author: windows-sdk-content
description: Gets the description of an update.
old-location: wua\iupdatehistoryentry_description.htm
old-project: wua_sdk
ms.assetid: 355d4623-a84e-4994-ad41-cb4237feeaab
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: Description property [Windows Update Agent], Description property [Windows Update Agent],IUpdateHistoryEntry interface, IUpdateHistoryEntry interface [Windows Update Agent],Description property, IUpdateHistoryEntry.Description, IUpdateHistoryEntry.get_Description, IUpdateHistoryEntry::Description, IUpdateHistoryEntry::get_Description, get_Description, wua.iupdatehistoryentry_description, wuapi/IUpdateHistoryEntry::Description, wuapi/IUpdateHistoryEntry::get_Description
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
 - IUpdateHistoryEntry.Description
 - IUpdateHistoryEntry.get_Description
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>



<a href="https://msdn.microsoft.com/7c2a209f-10e8-4158-8201-a062f86b5fdd">IUpdateHistoryEntry.ClientApplicationID</a>
 

 

