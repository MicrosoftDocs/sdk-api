---
UID: NF:wuapi.IUpdateHistoryEntry.get_UnmappedResultCode
title: IUpdateHistoryEntry::get_UnmappedResultCode (wuapi.h)
description: Gets the unmapped result code that is returned from an operation on an update.
helpviewer_keywords: ["IUpdateHistoryEntry interface [Windows Update Agent]","UnmappedResultCode property","IUpdateHistoryEntry.UnmappedResultCode","IUpdateHistoryEntry.get_UnmappedResultCode","IUpdateHistoryEntry::UnmappedResultCode","IUpdateHistoryEntry::get_UnmappedResultCode","UnmappedResultCode property [Windows Update Agent]","UnmappedResultCode property [Windows Update Agent]","IUpdateHistoryEntry interface","get_UnmappedResultCode","wua.iupdatehistoryentry_unmappedresultcode","wuapi/IUpdateHistoryEntry::UnmappedResultCode","wuapi/IUpdateHistoryEntry::get_UnmappedResultCode"]
old-location: wua\iupdatehistoryentry_unmappedresultcode.htm
tech.root: wua
ms.assetid: 8c0c49c2-6902-4c4b-95a9-5254b0b83897
ms.date: 12/05/2018
ms.keywords: IUpdateHistoryEntry interface [Windows Update Agent],UnmappedResultCode property, IUpdateHistoryEntry.UnmappedResultCode, IUpdateHistoryEntry.get_UnmappedResultCode, IUpdateHistoryEntry::UnmappedResultCode, IUpdateHistoryEntry::get_UnmappedResultCode, UnmappedResultCode property [Windows Update Agent], UnmappedResultCode property [Windows Update Agent],IUpdateHistoryEntry interface, get_UnmappedResultCode, wua.iupdatehistoryentry_unmappedresultcode, wuapi/IUpdateHistoryEntry::UnmappedResultCode, wuapi/IUpdateHistoryEntry::get_UnmappedResultCode
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
 - IUpdateHistoryEntry::get_UnmappedResultCode
 - wuapi/IUpdateHistoryEntry::get_UnmappedResultCode
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
 - IUpdateHistoryEntry.UnmappedResultCode
 - IUpdateHistoryEntry.get_UnmappedResultCode
---

# IUpdateHistoryEntry::get_UnmappedResultCode


## -description

Gets the unmapped result code that is returned from an operation on an update.

This property is read-only.

## -parameters

## -remarks

The returned value is an unmapped result code. To retrieve a mapped exception code, use the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_hresult">HResult</a> property.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_hresult">IUpdateHistoryEntry.HResult</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_operation">IUpdateHistoryEntry.Operation</a>