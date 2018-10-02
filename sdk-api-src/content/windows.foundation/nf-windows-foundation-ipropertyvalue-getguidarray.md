---
UID: NF:windows.foundation.IPropertyValue.GetGuidArray
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the array of Guid values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getguidarray.htm
tech.root: WinRT
ms.assetid: 83d19a18-3cd4-4343-8609-12e9a65b8e37
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetGuidArray, GetGuidArray method [Windows Runtime], GetGuidArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetGuidArray method, IPropertyValue.GetGuidArray, IPropertyValue.IPropertyValue, IPropertyValue::GetGuidArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetGuidArray, winrt.ipropertyvalue_getguidarray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IPropertyValue.GetGuidArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://msdn.microsoft.com/library/system.guid.aspx">Guid</a> values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize

TBD


### -param value [out]

Type: <b>GUID**</b>

The array of <a href="https://msdn.microsoft.com/library/system.guid.aspx">Guid</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/8284b582-2bba-4afd-9f8c-3b2169e0adbf">IPropertyValueStatics::CreateGuidArray</a>
 

 

