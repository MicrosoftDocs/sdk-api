---
UID: NF:wuapi.IUpdateHistoryEntry.get_ClientApplicationID
title: IUpdateHistoryEntry::get_ClientApplicationID (wuapi.h)
description: Gets the identifier of the client application that processed an update.
helpviewer_keywords: ["ClientApplicationID property [Windows Update Agent]","ClientApplicationID property [Windows Update Agent]","IUpdateHistoryEntry interface","IUpdateHistoryEntry interface [Windows Update Agent]","ClientApplicationID property","IUpdateHistoryEntry.ClientApplicationID","IUpdateHistoryEntry.get_ClientApplicationID","IUpdateHistoryEntry::ClientApplicationID","IUpdateHistoryEntry::get_ClientApplicationID","get_ClientApplicationID","wua.iupdatehistoryentry_clientapplicationid","wuapi/IUpdateHistoryEntry::ClientApplicationID","wuapi/IUpdateHistoryEntry::get_ClientApplicationID"]
old-location: wua\iupdatehistoryentry_clientapplicationid.htm
tech.root: wua
ms.assetid: 7c2a209f-10e8-4158-8201-a062f86b5fdd
ms.date: 12/05/2018
ms.keywords: ClientApplicationID property [Windows Update Agent], ClientApplicationID property [Windows Update Agent],IUpdateHistoryEntry interface, IUpdateHistoryEntry interface [Windows Update Agent],ClientApplicationID property, IUpdateHistoryEntry.ClientApplicationID, IUpdateHistoryEntry.get_ClientApplicationID, IUpdateHistoryEntry::ClientApplicationID, IUpdateHistoryEntry::get_ClientApplicationID, get_ClientApplicationID, wua.iupdatehistoryentry_clientapplicationid, wuapi/IUpdateHistoryEntry::ClientApplicationID, wuapi/IUpdateHistoryEntry::get_ClientApplicationID
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
 - IUpdateHistoryEntry::get_ClientApplicationID
 - wuapi/IUpdateHistoryEntry::get_ClientApplicationID
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
 - IUpdateHistoryEntry.ClientApplicationID
 - IUpdateHistoryEntry.get_ClientApplicationID
---

# IUpdateHistoryEntry::get_ClientApplicationID


## -description

Gets the identifier of the client application that processed an update.

This property is read-only.

## -parameters

## -remarks

Returns the Unknown value if the client application has not set the property.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>