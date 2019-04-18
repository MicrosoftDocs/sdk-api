---
UID: NF:windows.foundation.IPropertyValue.GetPointArray
title: IPropertyValue::IPropertyValue (windows.foundation.h)
author: windows-sdk-content
description: Gets the array of Point values that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getpointarray.htm
tech.root: WinRT
ms.assetid: 7df4ad4e-3ca6-4956-b907-02c2cb6e481b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPointArray, GetPointArray method [Windows Runtime], GetPointArray method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetPointArray method, IPropertyValue.GetPointArray, IPropertyValue.IPropertyValue, IPropertyValue::GetPointArray, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetPointArray, winrt.ipropertyvalue_getpointarray
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
 - IPropertyValue.GetPointArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValue::IPropertyValue


## -description


Gets the array of <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> values that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param __valueSize [out]

Type: <b>UINT32*</b>

The number of values in the array.


### -param value [out]

Type: <b><a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a>**</b>

The array of <a href="https://msdn.microsoft.com/0cdd5b17-2f7e-4e17-896c-7d7784c8643d">Point</a> values.

The returned pointer must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/cdfc2a91-0f1b-41d9-99e3-e3589bdae6ca">IPropertyValueStatics::CreatePointArray</a>
 

 

