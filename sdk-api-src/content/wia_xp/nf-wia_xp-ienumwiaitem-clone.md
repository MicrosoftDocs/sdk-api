---
UID: NF:wia_xp.IEnumWiaItem.Clone
title: IEnumWiaItem::Clone
author: windows-sdk-content
description: The IEnumWiaItem::Clone method creates an additional instance of the IEnumWiaItem interface and sends back a pointer to it.
old-location: wia\_wia_IEnumWiaItem_Clone.htm
old-project: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwiaitem\clone.htm
ms.author: windowssdkdev
ms.date: 05/03/2018
ms.keywords: Clone, Clone method [WIA], Clone method [WIA],IEnumWiaItem interface, IEnumWiaItem interface [WIA],Clone method, IEnumWiaItem.Clone, IEnumWiaItem::Clone, _wia_IEnumWiaItem_Clone, wia._wia_IEnumWiaItem_Clone, wia_xp/IEnumWiaItem::Clone
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaguid.lib
-	Wiaguid.dll
api_name:
-	IEnumWiaItem.Clone
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWiaItem::Clone


## -description


The <b>IEnumWiaItem::Clone</b> method creates an additional instance of the <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface and sends back a pointer to it.


## -parameters




### -param ppIEnum [out]

Type: <b><a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a>**</b>

Pointer  to the <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface. Receives the address of the <b>IEnumWiaItem</b> interface instance that <b>IEnumWiaItem::Clone</b> creates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppIEnum</i> parameter.



