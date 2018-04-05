---
UID: NF:wuapi.IUpdateHistoryEntry.get_UnmappedResultCode
title: IUpdateHistoryEntry::get_UnmappedResultCode method
author: windows-driver-content
description: Gets the unmapped result code that is returned from an operation on an update.
old-location: wua\iupdatehistoryentry_unmappedresultcode.htm
old-project: Wua_Sdk
ms.assetid: 8c0c49c2-6902-4c4b-95a9-5254b0b83897
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IUpdateHistoryEntry, IUpdateHistoryEntry interface [Windows Update Agent], UnmappedResultCode property, IUpdateHistoryEntry.UnmappedResultCode, IUpdateHistoryEntry::get_UnmappedResultCode, UnmappedResultCode property [Windows Update Agent], UnmappedResultCode property [Windows Update Agent], IUpdateHistoryEntry interface, get_UnmappedResultCode,IUpdateHistoryEntry.get_UnmappedResultCode, wua.iupdatehistoryentry_unmappedresultcode, wuapi/IUpdateHistoryEntry::UnmappedResultCode, wuapi/IUpdateHistoryEntry::get_UnmappedResultCode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateHistoryEntry.UnmappedResultCode
-	IUpdateHistoryEntry.get_UnmappedResultCode
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateHistoryEntry::get_UnmappedResultCode method


## -description


Gets the unmapped result code that is returned from an operation on an update.

This property is read-only.


## -parameters


## -remarks



The returned value is an unmapped result code. To retrieve a mapped exception code, use the <a href="https://msdn.microsoft.com/7e1968f9-548c-4002-848b-9443d12ea0a7">HResult</a> property.




## -see-also




<a href="https://msdn.microsoft.com/7f67ba11-41b5-4185-a78d-75c76dbe1fbe">IUpdateHistoryEntry</a>



<a href="https://msdn.microsoft.com/7e1968f9-548c-4002-848b-9443d12ea0a7">IUpdateHistoryEntry.HResult</a>



<a href="https://msdn.microsoft.com/4dfad46b-ee42-41d6-be25-69aaf12fd53c">IUpdateHistoryEntry.Operation</a>
 

 

