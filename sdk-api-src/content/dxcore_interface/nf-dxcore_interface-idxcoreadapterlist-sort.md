---
UID: NF:dxcore_interface.IDXCoreAdapterList.Sort
title: IDXCoreAdapterList::Sort
description: Sorts a DXCore adapter list object based on a provided input array of sort criteria.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,Sort method, IDXCoreAdapterFactory.Sort, IDXCoreAdapterFactory::Sort, Sort, Sort method, Sort method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::Sort, dxcore_interface.idxcoreadapterfactory_sort
ms.localizationpriority: low
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: method
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - COM
api_location:
 - dxcore.dll
api_name:
 - IDXCoreAdapterList::Sort
---

## -description

Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight. **Sort** helps you to more easily find your ideal adapter in an adapter list.

## -parameters

### -param numPreferences

Type: **uint32_t**

The number of elements that are in the array pointed to by the *preferences* parameter.

### -param preferences [in]

Type: **const [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference)\***

A pointer to a constant array of [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference) values, representing sort criteria.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.|

## -remarks

In cases where a provided [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail. Known **DXCoreAdapterPreference** values will still be considered in this case. To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported).

**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority. 

Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type. The internal logic for a type may develop as the OS develops.

When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable. So, calling [IDXCoreAdapterList::GetAdapter](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.

## -see-also

[IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)