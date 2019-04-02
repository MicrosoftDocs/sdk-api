---
UID: NF:d2d1.D2D1CreateFactory~r1
title: D2D1CreateFactory
ms.date: 01/30/19
ms.keywords: D2D1CreateFactory
ms.topic: language-reference
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

Type: <b><a href="https://msdn.microsoft.com/428053d3-7ea0-4b01-9924-4a31d8e018fb">D2D1_FACTORY_TYPE</a></b>

The threading model of the factory and the resources it creates.


### -param riid

Type: <b>REFIID</b>

A reference to the IID of <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> that is obtained by using __uuidof(ID2D1Factory).


### -param factory

Type: <b>void**</b>

When this method returns, contains the address to a pointer to the new factory.


## -returns

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.


## -remarks

## -see-also

