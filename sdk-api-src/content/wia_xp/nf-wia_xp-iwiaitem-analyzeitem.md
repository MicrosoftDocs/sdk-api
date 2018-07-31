---
UID: NF:wia_xp.IWiaItem.AnalyzeItem
title: IWiaItem::AnalyzeItem
author: windows-sdk-content
description: The IWiaItem::AnalyzeItem method causes the Windows Image Acquisition (WIA) hardware device to acquire and try to detect what data types are present.
old-location: wia\_wia_IWiaItem_AnalyzeItem.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\analyzeitem.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AnalyzeItem, AnalyzeItem method [WIA], AnalyzeItem method [WIA],IWiaItem interface, IWiaItem interface [WIA],AnalyzeItem method, IWiaItem.AnalyzeItem, IWiaItem::AnalyzeItem, _wia_IWiaItem_AnalyzeItem, wia._wia_IWiaItem_AnalyzeItem, wia_xp/IWiaItem::AnalyzeItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem.AnalyzeItem
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used with scanners to detect what type of data is on a page. When an application calls this method, the WIA hardware device driver scans and analyzes the current page. For each data type it detects, it creates an <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> object to represent the region on the page the data occupies. 

Image processing and OCR software can use this capability to detect graphics and text on a page. This method adds the regions it creates into the WIA device's <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> tree. The application can select the individual regions and use the standard data transfer methods to acquire data from them.

If necessary, applications can override the regions created by this method. 



