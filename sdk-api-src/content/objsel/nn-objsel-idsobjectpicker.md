---
UID: NN:objsel.IDsObjectPicker
title: IDsObjectPicker (objsel.h)
description: The IDsObjectPicker interface is used by an application to initialize and display an object picker dialog box. To create an instance of this interface, call CoCreateInstance with the CLSID_DsObjectPicker class identifier as shown below.
helpviewer_keywords: ["IDsObjectPicker","IDsObjectPicker interface [Active Directory]","IDsObjectPicker interface [Active Directory]","described","_glines_idsobjectpicker","ad.idsobjectpicker","objsel/IDsObjectPicker"]
old-location: ad\idsobjectpicker.htm
tech.root: ad
ms.assetid: f2f9da7d-7a09-4b49-a750-078a4573e213
ms.date: 12/05/2018
ms.keywords: IDsObjectPicker, IDsObjectPicker interface [Active Directory], IDsObjectPicker interface [Active Directory],described, _glines_idsobjectpicker, ad.idsobjectpicker, objsel/IDsObjectPicker
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Objsel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsObjectPicker
 - objsel/IDsObjectPicker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPicker
---

# IDsObjectPicker interface


## -description

The <b>IDsObjectPicker</b> interface is used by an application to initialize and display an object picker dialog box. To create an  instance of this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsObjectPicker</b> class identifier as shown below.

```cpp
HRESULT hr = S_OK;
IDsObjectPicker *pDsObjectPicker = NULL;
 
hr = CoCreateInstance(CLSID_DsObjectPicker,
             NULL,
             CLSCTX_INPROC_SERVER,
             IID_IDsObjectPicker,
             (void **) &pDsObjectPicker);
```

The  <b>IDsObjectPicker</b> implemented by the system  supports both apartment and free-threading models and is thread safe. In practice, this means that a call to the methods of this interface will block until no other thread of your application is calling any other method on that instance of the interface.

## -inheritance

The <b>IDsObjectPicker</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsObjectPicker</b> also has these types of members:

## -remarks

It is acceptable to create and initialize a single instance of the <b>IDsObjectPicker</b> interface and then make multiple 
calls to <a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-invokedialog">InvokeDialog</a> without having to reinitializing the interface.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>
