---
UID: NF:wia_xp.IEnumWiaItem.Skip
title: IEnumWiaItem::Skip
author: windows-driver-content
description: The IEnumWiaItem::Skip method skips the specified number of items during an enumeration of available IWiaItem objects.
old-location: wia\_wia_IEnumWiaItem_Skip.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\skip.htm
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IEnumWiaItem interface [WIA],Skip method, IEnumWiaItem.Skip, IEnumWiaItem::Skip, Skip, Skip method [WIA], Skip method [WIA],IEnumWiaItem interface, _wia_IEnumWiaItem_Skip, wia._wia_IEnumWiaItem_Skip, wia_xp/IEnumWiaItem::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IEnumWiaItem.Skip
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWiaItem::Skip


## -description


The <b>IEnumWiaItem::Skip</b> method skips the specified number of items during an enumeration of available <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of items to skip. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. If it is unable to skip the specified number of items, it returns S_FALSE. If the method fails, it returns a standard COM error code.



