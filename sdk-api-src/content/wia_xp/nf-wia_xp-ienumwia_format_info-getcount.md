---
UID: NF:wia_xp.IEnumWIA_FORMAT_INFO.GetCount
title: IEnumWIA_FORMAT_INFO::GetCount method
author: windows-driver-content
description: The IEnumWIA_FORMAT_INFO::GetCount method returns the number of elements stored by this enumerator.
old-location: wia\_wia_IEnumWIA_FORMAT_INFO_GetCount.htm
old-project: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwia_format_info\getcount.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetCount method [WIA], GetCount method [WIA], IEnumWIA_FORMAT_INFO interface, GetCount,IEnumWIA_FORMAT_INFO.GetCount, IEnumWIA_FORMAT_INFO, IEnumWIA_FORMAT_INFO interface [WIA], GetCount method, IEnumWIA_FORMAT_INFO::GetCount, _wia_IEnumWIA_FORMAT_INFO_GetCount, wia._wia_IEnumWIA_FORMAT_INFO_GetCount, wia_xp/IEnumWIA_FORMAT_INFO::GetCount
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
-	IEnumWIA_FORMAT_INFO.GetCount
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWIA_FORMAT_INFO::GetCount method


## -description


The <b>IEnumWIA_FORMAT_INFO::GetCount</b> method returns the number of elements stored by this enumerator.


## -parameters




### -param pcelt [out]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> that receives the number of elements in the enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



