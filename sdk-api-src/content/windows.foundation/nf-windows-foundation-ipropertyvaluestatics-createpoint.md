---
UID: NF:windows.foundation.IPropertyValueStatics.CreatePoint
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified Point value.
helpviewer_keywords: ["CreatePoint","CreatePoint method [Windows Runtime]","CreatePoint method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreatePoint method","IPropertyValueStatics.CreatePoint","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreatePoint","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreatePoint","winrt.ipropertyvaluefactory_createpoint","winrt.ipropertyvaluestatics_createpoint"]
old-location: winrt\ipropertyvaluestatics_createpoint.htm
tech.root: WinRT
ms.assetid: b4cf8b1b-1673-4ac0-a66d-d83b98eec741
ms.date: 12/05/2018
ms.keywords: CreatePoint, CreatePoint method [Windows Runtime], CreatePoint method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreatePoint method, IPropertyValueStatics.CreatePoint, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreatePoint, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreatePoint, winrt.ipropertyvaluefactory_createpoint, winrt.ipropertyvaluestatics_createpoint
f1_keywords:
- windows.foundation/IPropertyValueStatics.CreatePoint
dev_langs:
- c++
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.Foundation.h
api_name:
- IPropertyValueStatics.CreatePoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> value.


## -parameters




### -param value [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a></b>

The value to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getpoint">IPropertyValue::GetPoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
 

 

