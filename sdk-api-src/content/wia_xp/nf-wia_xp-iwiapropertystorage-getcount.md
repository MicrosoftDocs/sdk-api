---
UID: NF:wia_xp.IWiaPropertyStorage.GetCount
title: IWiaPropertyStorage::GetCount (wia_xp.h)
description: The IWiaPropertyStorage::GetCount method returns the number of properties stored in the property storage.
helpviewer_keywords: ["GetCount","GetCount method [WIA]","GetCount method [WIA]","IWiaPropertyStorage interface","IWiaPropertyStorage interface [WIA]","GetCount method","IWiaPropertyStorage.GetCount","IWiaPropertyStorage::GetCount","_wia_IWiaPropertyStorage_GetCount","wia._wia_IWiaPropertyStorage_GetCount","wia_xp/IWiaPropertyStorage::GetCount"]
old-location: wia\_wia_IWiaPropertyStorage_GetCount.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\getcount.htm
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [WIA], GetCount method [WIA],IWiaPropertyStorage interface, IWiaPropertyStorage interface [WIA],GetCount method, IWiaPropertyStorage.GetCount, IWiaPropertyStorage::GetCount, _wia_IWiaPropertyStorage_GetCount, wia._wia_IWiaPropertyStorage_GetCount, wia_xp/IWiaPropertyStorage::GetCount
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
 - IWiaPropertyStorage::GetCount
 - wia_xp/IWiaPropertyStorage::GetCount
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
 - IWiaPropertyStorage.GetCount
archived: true
---

# IWiaPropertyStorage::GetCount


## -description

The <b>IWiaPropertyStorage::GetCount</b> method returns the number of properties stored in the property storage.

## -parameters

### -param pulNumProps [out]

Type: <b>ULONG*</b>

Receives the number of properties stored in the property storage.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a>