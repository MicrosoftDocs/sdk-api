---
UID: NF:wuapi.IUpdateHistoryEntry.get_HResult
title: IUpdateHistoryEntry::get_HResult (wuapi.h)
description: Gets the HRESULT value that is returned from the operation on an update.
helpviewer_keywords: ["HResult property [Windows Update Agent]","HResult property [Windows Update Agent]","IUpdateHistoryEntry interface","IUpdateHistoryEntry interface [Windows Update Agent]","HResult property","IUpdateHistoryEntry.HResult","IUpdateHistoryEntry.get_HResult","IUpdateHistoryEntry::HResult","IUpdateHistoryEntry::get_HResult","get_HResult","wua.iupdatehistoryentry_hresult","wuapi/IUpdateHistoryEntry::HResult","wuapi/IUpdateHistoryEntry::get_HResult"]
old-location: wua\iupdatehistoryentry_hresult.htm
tech.root: wua
ms.assetid: 7e1968f9-548c-4002-848b-9443d12ea0a7
ms.date: 12/05/2018
ms.keywords: HResult property [Windows Update Agent], HResult property [Windows Update Agent],IUpdateHistoryEntry interface, IUpdateHistoryEntry interface [Windows Update Agent],HResult property, IUpdateHistoryEntry.HResult, IUpdateHistoryEntry.get_HResult, IUpdateHistoryEntry::HResult, IUpdateHistoryEntry::get_HResult, get_HResult, wua.iupdatehistoryentry_hresult, wuapi/IUpdateHistoryEntry::HResult, wuapi/IUpdateHistoryEntry::get_HResult
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
 - IUpdateHistoryEntry::get_HResult
 - wuapi/IUpdateHistoryEntry::get_HResult
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
 - IUpdateHistoryEntry.HResult
 - IUpdateHistoryEntry.get_HResult
---

# IUpdateHistoryEntry::get_HResult


## -description

Gets the <b>HRESULT</b> value that is returned from the operation on an update.

This property is read-only.

## -parameters

## -remarks

The returned value is a mapped exception code. To retrieve the actual exception code, use the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode">UnmappedResultCode</a> property.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentry">IUpdateHistoryEntry</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode">UnmappedResultCode</a>