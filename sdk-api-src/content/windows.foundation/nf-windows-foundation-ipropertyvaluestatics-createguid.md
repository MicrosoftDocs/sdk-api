---
UID: NF:windows.foundation.IPropertyValueStatics.CreateGuid
title: IPropertyValueStatics::CreateGuid (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified GUID value.
helpviewer_keywords: ["CreateGuid","CreateGuid method [Windows Runtime]","CreateGuid method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateGuid method","IPropertyValueStatics.CreateGuid","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateGuid","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateGuid","winrt.ipropertyvaluefactory_createguid","winrt.ipropertyvaluestatics_createguid"]
old-location: winrt\ipropertyvaluestatics_createguid.htm
tech.root: WinRT
ms.assetid: fb895839-953f-41e2-963a-26156c490df0
ms.date: 12/05/2018
ms.keywords: CreateGuid, CreateGuid method [Windows Runtime], CreateGuid method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateGuid method, IPropertyValueStatics.CreateGuid, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateGuid, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateGuid, winrt.ipropertyvaluefactory_createguid, winrt.ipropertyvaluestatics_createguid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyValueStatics::CreateGuid
 - windows.foundation/IPropertyValueStatics::CreateGuid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValueStatics.CreateGuid
---

# IPropertyValueStatics::CreateGuid (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified <b>GUID</b> value.

## -parameters

### -param value [in]

Type: <b>GUID</b>

The value to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getguid">IPropertyValue::GetGuid</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
