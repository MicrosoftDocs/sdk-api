---
UID: NF:wia_xp.IEnumWiaItem.GetCount
title: IEnumWiaItem::GetCount
author: windows-sdk-content
description: The IEnumWiaItem::GetCount method returns the number of elements stored by this enumerator.
old-location: wia\_wia_IEnumWiaItem_GetCount.htm
old-project: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwiaitem\getcount.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCount, GetCount method [WIA], GetCount method [WIA],IEnumWiaItem interface, IEnumWiaItem interface [WIA],GetCount method, IEnumWiaItem.GetCount, IEnumWiaItem::GetCount, _wia_IEnumWiaItem_GetCount, wia._wia_IEnumWiaItem_GetCount, wia_xp/IEnumWiaItem::GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWiaItem.GetCount
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWiaItem::GetCount


## -description


The <b>IEnumWiaItem::GetCount</b> method returns the number of elements stored by this enumerator.


## -parameters




### -param celt [out]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> that receives the number of elements in the enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



