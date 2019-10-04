---
UID: NF:wuapi.IUpdateHistoryEntry.get_ServiceID
title: IUpdateHistoryEntry::get_ServiceID (wuapi.h)
author: windows-sdk-content
description: Gets the service identifier of an update service that is not a Windows update.
old-location: wua\iupdatehistoryentry_serviceid.htm
tech.root: Wua_Sdk
ms.assetid: 01e430fa-6ff6-47f9-bac7-7d611b0f934f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],ServiceID property, IUpdateHistoryEntry.ServiceID, IUpdateHistoryEntry.get_ServiceID, IUpdateHistoryEntry::ServiceID, IUpdateHistoryEntry::get_ServiceID, ServiceID property [Windows Update Agent], ServiceID property [Windows Update Agent],IUpdateHistoryEntry interface, get_ServiceID, wua.iupdatehistoryentry_serviceid, wuapi/IUpdateHistoryEntry::ServiceID, wuapi/IUpdateHistoryEntry::get_ServiceID
ms.topic: method
f1_keywords: 
 - "wuapi/IUpdateHistoryEntry.ServiceID"
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
 - IUpdateHistoryEntry.ServiceID
 - IUpdateHistoryEntry.get_ServiceID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateHistoryEntry::get_ServiceID


## -description


Gets the service identifier of an update service that is not a Windows update. This property is meaningful only if the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection">ServerSelection</a> property returns <b>ssOthers</b>.

This property is read-only.


## -parameters


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>
 

 

