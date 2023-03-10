---
UID: NF:wuapi.IUpdateHistoryEntry.get_UninstallationSteps
title: IUpdateHistoryEntry::get_UninstallationSteps (wuapi.h)
description: Gets the IStringCollection interface that contains the uninstallation steps for an update.
helpviewer_keywords: ["IUpdateHistoryEntry interface [Windows Update Agent]","UninstallationSteps property","IUpdateHistoryEntry.UninstallationSteps","IUpdateHistoryEntry.get_UninstallationSteps","IUpdateHistoryEntry::UninstallationSteps","IUpdateHistoryEntry::get_UninstallationSteps","UninstallationSteps property [Windows Update Agent]","UninstallationSteps property [Windows Update Agent]","IUpdateHistoryEntry interface","get_UninstallationSteps","wua.iupdatehistoryentry_uninstallationsteps","wuapi/IUpdateHistoryEntry::UninstallationSteps","wuapi/IUpdateHistoryEntry::get_UninstallationSteps"]
old-location: wua\iupdatehistoryentry_uninstallationsteps.htm
tech.root: wua
ms.assetid: 28c3db7b-a212-40d8-8557-02509675db5a
ms.date: 12/05/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],UninstallationSteps property, IUpdateHistoryEntry.UninstallationSteps, IUpdateHistoryEntry.get_UninstallationSteps, IUpdateHistoryEntry::UninstallationSteps, IUpdateHistoryEntry::get_UninstallationSteps, UninstallationSteps property [Windows Update Agent], UninstallationSteps property [Windows Update Agent],IUpdateHistoryEntry interface, get_UninstallationSteps, wua.iupdatehistoryentry_uninstallationsteps, wuapi/IUpdateHistoryEntry::UninstallationSteps, wuapi/IUpdateHistoryEntry::get_UninstallationSteps
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
 - IUpdateHistoryEntry::get_UninstallationSteps
 - wuapi/IUpdateHistoryEntry::get_UninstallationSteps
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
 - IUpdateHistoryEntry.UninstallationSteps
 - IUpdateHistoryEntry.get_UninstallationSteps
---

# IUpdateHistoryEntry::get_UninstallationSteps


## -description

Gets the <a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a> interface that contains the uninstallation steps for an update.

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