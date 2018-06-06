---
UID: NF:wuapi.IUpdateHistoryEntry.get_ServiceID
title: IUpdateHistoryEntry::get_ServiceID
author: windows-sdk-content
description: Gets the service identifier of an update service that is not a Windows update.
old-location: wua\iupdatehistoryentry_serviceid.htm
old-project: Wua_Sdk
ms.assetid: 01e430fa-6ff6-47f9-bac7-7d611b0f934f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],ServiceID property, IUpdateHistoryEntry.ServiceID, IUpdateHistoryEntry.get_ServiceID, IUpdateHistoryEntry::ServiceID, IUpdateHistoryEntry::get_ServiceID, ServiceID property [Windows Update Agent], ServiceID property [Windows Update Agent],IUpdateHistoryEntry interface, get_ServiceID, wua.iupdatehistoryentry_serviceid, wuapi/IUpdateHistoryEntry::ServiceID, wuapi/IUpdateHistoryEntry::get_ServiceID
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
 - IUpdateHistoryEntry.ServiceID
 - IUpdateHistoryEntry.get_ServiceID
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateHistoryEntry::get_ServiceID


## -description


Gets the service identifier of an update service that is not a Windows update. This property is meaningful only if the <a href="https://msdn.microsoft.com/26b1c4ce-edc0-46cb-80f7-6a140df9c88b">ServerSelection</a> property returns <b>ssOthers</b>.

This property is read-only.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>
 

 

