---
UID: NF:wuapi.IUpdateHistoryEntry.get_ServiceID
title: IUpdateHistoryEntry::get_ServiceID (wuapi.h)
description: Gets the service identifier of an update service that is not a Windows update.
helpviewer_keywords: ["IUpdateHistoryEntry interface [Windows Update Agent]","ServiceID property","IUpdateHistoryEntry.ServiceID","IUpdateHistoryEntry.get_ServiceID","IUpdateHistoryEntry::ServiceID","IUpdateHistoryEntry::get_ServiceID","ServiceID property [Windows Update Agent]","ServiceID property [Windows Update Agent]","IUpdateHistoryEntry interface","get_ServiceID","wua.iupdatehistoryentry_serviceid","wuapi/IUpdateHistoryEntry::ServiceID","wuapi/IUpdateHistoryEntry::get_ServiceID"]
old-location: wua\iupdatehistoryentry_serviceid.htm
tech.root: wua
ms.assetid: 01e430fa-6ff6-47f9-bac7-7d611b0f934f
ms.date: 12/05/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],ServiceID property, IUpdateHistoryEntry.ServiceID, IUpdateHistoryEntry.get_ServiceID, IUpdateHistoryEntry::ServiceID, IUpdateHistoryEntry::get_ServiceID, ServiceID property [Windows Update Agent], ServiceID property [Windows Update Agent],IUpdateHistoryEntry interface, get_ServiceID, wua.iupdatehistoryentry_serviceid, wuapi/IUpdateHistoryEntry::ServiceID, wuapi/IUpdateHistoryEntry::get_ServiceID
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
 - IUpdateHistoryEntry::get_ServiceID
 - wuapi/IUpdateHistoryEntry::get_ServiceID
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
 - IUpdateHistoryEntry.ServiceID
 - IUpdateHistoryEntry.get_ServiceID
---

# IUpdateHistoryEntry::get_ServiceID


## -description

Gets the service identifier of an update service that is not a Windows update. This property is meaningful only if the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection">ServerSelection</a> property returns <b>ssOthers</b>.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>