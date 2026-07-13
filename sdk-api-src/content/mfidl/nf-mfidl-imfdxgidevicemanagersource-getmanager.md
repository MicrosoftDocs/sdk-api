---
UID: NF:mfidl.IMFDXGIDeviceManagerSource.GetManager
title: IMFDXGIDeviceManagerSource::GetManager (mfidl.h)
description: Gets the IMFDXGIDeviceManager from the Microsoft Media Foundation video rendering sink.
helpviewer_keywords: ["GetManager","GetManager method [Media Foundation]","GetManager method [Media Foundation]","IMFDXGIDeviceManagerSource interface","IMFDXGIDeviceManagerSource interface [Media Foundation]","GetManager method","IMFDXGIDeviceManagerSource.GetManager","IMFDXGIDeviceManagerSource::GetManager","mf.imfdxgidevicemanagersource_getmanager","mfidl/IMFDXGIDeviceManagerSource::GetManager"]
old-location: mf\imfdxgidevicemanagersource_getmanager.htm
tech.root: mf
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
ms.date: 12/05/2018
ms.keywords: GetManager, GetManager method [Media Foundation], GetManager method [Media Foundation],IMFDXGIDeviceManagerSource interface, IMFDXGIDeviceManagerSource interface [Media Foundation],GetManager method, IMFDXGIDeviceManagerSource.GetManager, IMFDXGIDeviceManagerSource::GetManager, mf.imfdxgidevicemanagersource_getmanager, mfidl/IMFDXGIDeviceManagerSource::GetManager
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDXGIDeviceManagerSource::GetManager
 - mfidl/IMFDXGIDeviceManagerSource::GetManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFDXGIDeviceManagerSource.GetManager
---

# IMFDXGIDeviceManagerSource::GetManager


## -description

Gets the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> from the Microsoft Media Foundation video rendering sink.

## -parameters

### -param ppManager [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/imfdxgidevicemanagersource">IMFDXGIDeviceManagerSource</a>