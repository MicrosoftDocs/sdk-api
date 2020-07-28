---
UID: NF:wia_xp.IEnumWIA_FORMAT_INFO.GetCount
title: IEnumWIA_FORMAT_INFO::GetCount (wia_xp.h)
description: The IEnumWIA_FORMAT_INFO::GetCount method returns the number of elements stored by this enumerator.
helpviewer_keywords: ["GetCount","GetCount method [WIA]","GetCount method [WIA]","IEnumWIA_FORMAT_INFO interface","IEnumWIA_FORMAT_INFO interface [WIA]","GetCount method","IEnumWIA_FORMAT_INFO.GetCount","IEnumWIA_FORMAT_INFO::GetCount","_wia_IEnumWIA_FORMAT_INFO_GetCount","wia._wia_IEnumWIA_FORMAT_INFO_GetCount","wia_xp/IEnumWIA_FORMAT_INFO::GetCount"]
old-location: wia\_wia_IEnumWIA_FORMAT_INFO_GetCount.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\wiax\refwia\ifaces\ienumwia_format_info\getcount.htm
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [WIA], GetCount method [WIA],IEnumWIA_FORMAT_INFO interface, IEnumWIA_FORMAT_INFO interface [WIA],GetCount method, IEnumWIA_FORMAT_INFO.GetCount, IEnumWIA_FORMAT_INFO::GetCount, _wia_IEnumWIA_FORMAT_INFO_GetCount, wia._wia_IEnumWIA_FORMAT_INFO_GetCount, wia_xp/IEnumWIA_FORMAT_INFO::GetCount
f1_keywords:
- wia_xp/IEnumWIA_FORMAT_INFO.GetCount
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
api_name:
- IEnumWIA_FORMAT_INFO.GetCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumWIA_FORMAT_INFO::GetCount


## -description


The <b>IEnumWIA_FORMAT_INFO::GetCount</b> method returns the number of elements stored by this enumerator.


## -parameters




### -param pcelt [out]

Type: <b>ULONG*</b>

Pointer to a <b>ULONG</b> that receives the number of elements in the enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



