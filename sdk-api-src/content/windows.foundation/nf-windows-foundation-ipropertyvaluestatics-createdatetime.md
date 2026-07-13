---
UID: NF:windows.foundation.IPropertyValueStatics.CreateDateTime
title: IPropertyValueStatics::CreateDateTime (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified DateTime value.
helpviewer_keywords: ["CreateDateTime","CreateDateTime method [Windows Runtime]","CreateDateTime method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateDateTime method","IPropertyValueStatics.CreateDateTime","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateDateTime","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateDateTime","winrt.ipropertyvaluefactory_createdatetime","winrt.ipropertyvaluestatics_createdatetime"]
old-location: winrt\ipropertyvaluestatics_createdatetime.htm
tech.root: WinRT
ms.assetid: d7191a38-df9e-4e19-a128-35260bbbfba9
ms.date: 12/05/2018
ms.keywords: CreateDateTime, CreateDateTime method [Windows Runtime], CreateDateTime method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateDateTime method, IPropertyValueStatics.CreateDateTime, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateDateTime, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateDateTime, winrt.ipropertyvaluefactory_createdatetime, winrt.ipropertyvaluestatics_createdatetime
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
 - IPropertyValueStatics::CreateDateTime
 - windows.foundation/IPropertyValueStatics::CreateDateTime
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
 - IPropertyValueStatics.CreateDateTime
---

# IPropertyValueStatics::CreateDateTime (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> value.

## -parameters

### -param value [in]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a></b>

The value to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetime">IPropertyValue::GetDateTime</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
