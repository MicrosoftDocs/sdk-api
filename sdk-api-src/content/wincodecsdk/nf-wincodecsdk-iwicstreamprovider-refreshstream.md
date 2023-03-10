---
UID: NF:wincodecsdk.IWICStreamProvider.RefreshStream
title: IWICStreamProvider::RefreshStream (wincodecsdk.h)
description: Informs the component that the content of the stream it's holding onto may have changed. The component should respond by dirtying any cached information from the stream.
helpviewer_keywords: ["IWICStreamProvider interface [Windows Imaging Component]","RefreshStream method","IWICStreamProvider.RefreshStream","IWICStreamProvider::RefreshStream","RefreshStream","RefreshStream method [Windows Imaging Component]","RefreshStream method [Windows Imaging Component]","IWICStreamProvider interface","_wic_codec_iwicstreamprovider_refreshstream","wic._wic_codec_iwicstreamprovider_refreshstream","wincodecsdk/IWICStreamProvider::RefreshStream"]
old-location: wic\_wic_codec_iwicstreamprovider_refreshstream.htm
tech.root: wic
ms.assetid: 47ee9b2a-b979-4009-b4e6-e2e39548976d
ms.date: 12/05/2018
ms.keywords: IWICStreamProvider interface [Windows Imaging Component],RefreshStream method, IWICStreamProvider.RefreshStream, IWICStreamProvider::RefreshStream, RefreshStream, RefreshStream method [Windows Imaging Component], RefreshStream method [Windows Imaging Component],IWICStreamProvider interface, _wic_codec_iwicstreamprovider_refreshstream, wic._wic_codec_iwicstreamprovider_refreshstream, wincodecsdk/IWICStreamProvider::RefreshStream
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICStreamProvider::RefreshStream
 - wincodecsdk/IWICStreamProvider::RefreshStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStreamProvider.RefreshStream
---

# IWICStreamProvider::RefreshStream


## -description

Informs the component that the content of the stream it's holding onto may have changed. The component should respond by dirtying any cached information from the stream.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

