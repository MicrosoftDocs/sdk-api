---
UID: NF:wia_xp.IWiaItem.AnalyzeItem
title: IWiaItem::AnalyzeItem (wia_xp.h)
description: The IWiaItem::AnalyzeItem method causes the Windows Image Acquisition (WIA) hardware device to acquire and try to detect what data types are present.
helpviewer_keywords: ["AnalyzeItem","AnalyzeItem method [WIA]","AnalyzeItem method [WIA]","IWiaItem interface","IWiaItem interface [WIA]","AnalyzeItem method","IWiaItem.AnalyzeItem","IWiaItem::AnalyzeItem","_wia_IWiaItem_AnalyzeItem","wia._wia_IWiaItem_AnalyzeItem","wia_xp/IWiaItem::AnalyzeItem"]
old-location: wia\_wia_IWiaItem_AnalyzeItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\analyzeitem.htm
ms.date: 12/05/2018
ms.keywords: AnalyzeItem, AnalyzeItem method [WIA], AnalyzeItem method [WIA],IWiaItem interface, IWiaItem interface [WIA],AnalyzeItem method, IWiaItem.AnalyzeItem, IWiaItem::AnalyzeItem, _wia_IWiaItem_AnalyzeItem, wia._wia_IWiaItem_AnalyzeItem, wia_xp/IWiaItem::AnalyzeItem
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaItem::AnalyzeItem
 - wia_xp/IWiaItem::AnalyzeItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.AnalyzeItem
archived: true
---

# IWiaItem::AnalyzeItem


## -description

The <b>IWiaItem::AnalyzeItem</b> method causes the Windows Image Acquisition (WIA) hardware device to acquire and try to detect what data types are present.

## -parameters

### -param lFlags [in]

Type: <b>LONG</b>

Currently unused. Should be set to zero.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used with scanners to detect what type of data is on a page. When an application calls this method, the WIA hardware device driver scans and analyzes the current page. For each data type it detects, it creates an <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> object to represent the region on the page the data occupies. 

Image processing and OCR software can use this capability to detect graphics and text on a page. This method adds the regions it creates into the WIA device's <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> tree. The application can select the individual regions and use the standard data transfer methods to acquire data from them.

If necessary, applications can override the regions created by this method.