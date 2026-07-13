---
UID: NF:wia_xp.IWiaPropertyStorage.GetPropertyStream
title: IWiaPropertyStorage::GetPropertyStream (wia_xp.h)
description: The IWiaPropertyStorage::GetPropertyStream method retrieves the property stream of an item.
helpviewer_keywords: ["GetPropertyStream","GetPropertyStream method [WIA]","GetPropertyStream method [WIA]","IWiaPropertyStorage interface","IWiaPropertyStorage interface [WIA]","GetPropertyStream method","IWiaPropertyStorage.GetPropertyStream","IWiaPropertyStorage::GetPropertyStream","_wia_IWiaPropertyStorage_GetPropertyStream","wia._wia_IWiaPropertyStorage_GetPropertyStream","wia_xp/IWiaPropertyStorage::GetPropertyStream"]
old-location: wia\_wia_IWiaPropertyStorage_GetPropertyStream.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\getpropertystream.htm
ms.date: 12/05/2018
ms.keywords: GetPropertyStream, GetPropertyStream method [WIA], GetPropertyStream method [WIA],IWiaPropertyStorage interface, IWiaPropertyStorage interface [WIA],GetPropertyStream method, IWiaPropertyStorage.GetPropertyStream, IWiaPropertyStorage::GetPropertyStream, _wia_IWiaPropertyStorage_GetPropertyStream, wia._wia_IWiaPropertyStorage_GetPropertyStream, wia_xp/IWiaPropertyStorage::GetPropertyStream
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
 - IWiaPropertyStorage::GetPropertyStream
 - wia_xp/IWiaPropertyStorage::GetPropertyStream
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
 - IWiaPropertyStorage.GetPropertyStream
archived: true
---

# IWiaPropertyStorage::GetPropertyStream


## -description

The <b>IWiaPropertyStorage::GetPropertyStream</b> method retrieves the property stream of an item.

## -parameters

### -param pCompatibilityId [out]

Type: <b>GUID*</b>

Receives a unique identifier for a set of property values.

### -param ppIStream [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

Pointer to a stream that receives the item properties. For more information, see <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications use this method to get a snapshot of the current properties of an item. These are subsequently restored by calling <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream">IWiaPropertyStorage::SetPropertyStream</a>.

Applications can use the <i>pCompatibilityID</i> parameter to check if a device supports a specific set of property values before attempting to write these values to the device.

When it is finished using the item's property stream, the application must release it.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a>