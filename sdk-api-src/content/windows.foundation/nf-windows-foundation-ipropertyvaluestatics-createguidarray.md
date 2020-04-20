---
UID: NF:windows.foundation.IPropertyValueStatics.CreateGuidArray
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of Guid values.helpviewer_keywords: ["CreateGuidArray","CreateGuidArray method [Windows Runtime]","CreateGuidArray method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateGuidArray method","IPropertyValueStatics.CreateGuidArray","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateGuidArray","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateGuidArray","winrt.ipropertyvaluefactory_createguidarray","winrt.ipropertyvaluestatics_createguidarray"]
old-location: winrt\ipropertyvaluestatics_createguidarray.htm
tech.root: WinRT
ms.assetid: 8284b582-2bba-4afd-9f8c-3b2169e0adbf
ms.date: 12/05/2018
ms.keywords: CreateGuidArray, CreateGuidArray method [Windows Runtime], CreateGuidArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateGuidArray method, IPropertyValueStatics.CreateGuidArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateGuidArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateGuidArray, winrt.ipropertyvaluefactory_createguidarray, winrt.ipropertyvaluestatics_createguidarray
f1_keywords:
- windows.foundation/IPropertyValueStatics.CreateGuidArray
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
- IPropertyValueStatics.CreateGuidArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of <a href="https://docs.microsoft.com/dotnet/api/system.guid?redirectedfrom=MSDN">Guid</a> values.


## -parameters




### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.


### -param value [in]

Type: <b>GUID*</b>

The array of <a href="https://docs.microsoft.com/dotnet/api/system.guid?redirectedfrom=MSDN">Guid</a> values to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getguidarray">IPropertyValue::GetGuidArray</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
 

 

