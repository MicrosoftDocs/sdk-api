---
UID: NF:windows.foundation.IPropertyValue.GetTimeSpanArray
title: IPropertyValue::GetTimeSpanArray method
author: windows-driver-content
description: Gets the array of TimeSpan values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_gettimespanarray.htm
old-project: WinRT
ms.assetid: a52a665c-4c3a-4489-bd7b-e8ecb8dfe9cc
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetTimeSpanArray method [Windows Runtime], GetTimeSpanArray method [Windows Runtime], IPropertyValue interface, GetTimeSpanArray,IPropertyValue.GetTimeSpanArray, IPropertyValue, IPropertyValue interface [Windows Runtime], GetTimeSpanArray method, IPropertyValue::GetTimeSpanArray, windows/IPropertyValue::GetTimeSpanArray, winrt.ipropertyvalue_gettimespanarray
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.Foundation.h
api_name:
-	IPropertyValue.GetTimeSpanArray
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValue::GetTimeSpanArray method


## -description


Gets the array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values that is stored in the current <a href="https://msdn.microsoft.com/29a8e6e5-764b-4de9-84ea-97abdee6b02f">IPropertyValue</a> object.


## -parameters




### -param __valueSize




### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a>**</b>

The array of <a href="https://msdn.microsoft.com/fbc6ecc2-6372-4b15-9532-3cd68a72e7b4">TimeSpan</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - length [out]

Type: <b>UINT32*</b>

The number of values in the array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/3f663acc-5ced-4fd2-a0d5-3e462fe60251">IPropertyValueStatics::CreateTimeSpanArray</a>
 

 

