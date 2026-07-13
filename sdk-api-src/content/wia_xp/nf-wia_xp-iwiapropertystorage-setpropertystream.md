---
UID: NF:wia_xp.IWiaPropertyStorage.SetPropertyStream
title: IWiaPropertyStorage::SetPropertyStream (wia_xp.h)
description: The IWiaPropertyStorage::SetPropertyStream sets the property stream of an item in the tree of IWiaItem objects of a Windows Image Acquisition (WIA) hardware device.
helpviewer_keywords: ["IWiaPropertyStorage interface [WIA]","SetPropertyStream method","IWiaPropertyStorage.SetPropertyStream","IWiaPropertyStorage::SetPropertyStream","SetPropertyStream","SetPropertyStream method [WIA]","SetPropertyStream method [WIA]","IWiaPropertyStorage interface","_wia_IWiaPropertyStorage_SetPropertyStream","wia._wia_IWiaPropertyStorage_SetPropertyStream","wia_xp/IWiaPropertyStorage::SetPropertyStream"]
old-location: wia\_wia_IWiaPropertyStorage_SetPropertyStream.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\setpropertystream.htm
ms.date: 12/05/2018
ms.keywords: IWiaPropertyStorage interface [WIA],SetPropertyStream method, IWiaPropertyStorage.SetPropertyStream, IWiaPropertyStorage::SetPropertyStream, SetPropertyStream, SetPropertyStream method [WIA], SetPropertyStream method [WIA],IWiaPropertyStorage interface, _wia_IWiaPropertyStorage_SetPropertyStream, wia._wia_IWiaPropertyStorage_SetPropertyStream, wia_xp/IWiaPropertyStorage::SetPropertyStream
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
 - IWiaPropertyStorage::SetPropertyStream
 - wia_xp/IWiaPropertyStorage::SetPropertyStream
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
 - IWiaPropertyStorage.SetPropertyStream
archived: true
---

# IWiaPropertyStorage::SetPropertyStream


## -description

The <b>IWiaPropertyStorage::SetPropertyStream</b> sets the property stream of an item in the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem">IWiaItem</a> objects of a Windows Image Acquisition (WIA) hardware device.

## -parameters

### -param pCompatibilityId [in]

Type: <b>GUID*</b>

Specifies a unique identifier for a set of property values.

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to the property stream that is used to set the current item's property stream.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications use the <i>pCompatibilityID</i> parameter to check whether a device supports a specific set of property values before attempting to write these values to the device.

Set <i>pIStream</i> to <b>NULL</b> to check whether the device driver accepts the CompatibilityID specified by <i>pCompatibilityID</i>.

If the application obtained the property stream of the item using the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream">IWiaPropertyStorage::GetPropertyStream</a> method, the application must release it. For more information, see <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a>