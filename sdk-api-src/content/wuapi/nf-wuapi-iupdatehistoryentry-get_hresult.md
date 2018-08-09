---
UID: NF:wuapi.IUpdateHistoryEntry.get_HResult
title: IUpdateHistoryEntry::get_HResult
author: windows-sdk-content
description: Gets the HRESULT value that is returned from the operation on an update.
old-location: wua\iupdatehistoryentry_hresult.htm
old-project: wua_sdk
ms.assetid: 7e1968f9-548c-4002-848b-9443d12ea0a7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: HResult property [Windows Update Agent], HResult property [Windows Update Agent],IUpdateHistoryEntry interface, IUpdateHistoryEntry interface [Windows Update Agent],HResult property, IUpdateHistoryEntry.HResult, IUpdateHistoryEntry.get_HResult, IUpdateHistoryEntry::HResult, IUpdateHistoryEntry::get_HResult, get_HResult, wua.iupdatehistoryentry_hresult, wuapi/IUpdateHistoryEntry::HResult, wuapi/IUpdateHistoryEntry::get_HResult
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
 - IUpdateHistoryEntry.HResult
 - IUpdateHistoryEntry.get_HResult
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateHistoryEntry::get_HResult


## -description


Gets the <b>HRESULT</b> value that is returned from the operation on an update.

This property is read-only.


## -parameters


## -remarks



The returned value is a mapped exception code. To retrieve the actual exception code, use the <a href="https://msdn.microsoft.com/8c0c49c2-6902-4c4b-95a9-5254b0b83897">UnmappedResultCode</a> property.




## -see-also




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>



<a href="https://msdn.microsoft.com/8c0c49c2-6902-4c4b-95a9-5254b0b83897">UnmappedResultCode</a>
 

 

