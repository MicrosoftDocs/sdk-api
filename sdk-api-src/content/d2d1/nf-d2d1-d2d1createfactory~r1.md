---
UID: NF:d2d1.D2D1CreateFactory~r1
title: D2D1CreateFactory
ms.date: 01/30/19
ms.keywords: D2D1CreateFactory
ms.topic: language-reference
f1_keywords: ["d2d1/D2D1CreateFactory"]
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d2d1.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - d2d1.h
api_name:
 - D2D1CreateFactory
---

# D2D1CreateFactory function


## -description

Creates a factory object that can be used to create Direct2D resources.


## -parameters

### -param factoryType

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type">D2D1_FACTORY_TYPE</a></b>

The threading model of the factory and the resources it creates.


### -param riid

Type: <b>REFIID</b>

A reference to the IID of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> that is obtained by using __uuidof(ID2D1Factory).


### -param factory

Type: <b>void**</b>

When this method returns, contains the address to a pointer to the new factory.


## -returns

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## -remarks

## -see-also

