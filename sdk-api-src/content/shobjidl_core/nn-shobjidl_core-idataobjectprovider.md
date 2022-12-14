---
UID: NN:shobjidl_core.IDataObjectProvider
title: IDataObjectProvider (shobjidl_core.h)
description: Provides methods that enable you to set or retrieve a DataPackage object's IDataObject interface, which the DataPackage uses to support interoperability. The DataPackage object is used by an app to provide data to another app.
helpviewer_keywords: ["IDataObjectProvider","IDataObjectProvider interface [Windows Shell]","IDataObjectProvider interface [Windows Shell]","described","shell.IDataObjectProvider","shobjidl_core/IDataObjectProvider"]
old-location: shell\IDataObjectProvider.htm
tech.root: shell
ms.assetid: 57A5003A-11DF-42c2-9C00-7DE35898B64D
ms.date: 12/05/2018
ms.keywords: IDataObjectProvider, IDataObjectProvider interface [Windows Shell], IDataObjectProvider interface [Windows Shell],described, shell.IDataObjectProvider, shobjidl_core/IDataObjectProvider
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IDataObjectProvider
 - shobjidl_core/IDataObjectProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDataObjectProvider
---

# IDataObjectProvider interface


## -description

Provides methods that enable you to set or retrieve a <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage">DataPackage</a> object's <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject interface</a>, which the DataPackage uses to support interoperability. The DataPackage object is used by an app to provide data to another app.

## -inheritance

The <b>IDataObjectProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataObjectProvider</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
Do not implement this interface. An implementation is provided as part of the DataPackage object.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
