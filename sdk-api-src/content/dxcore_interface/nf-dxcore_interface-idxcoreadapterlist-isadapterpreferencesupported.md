---
UID: NF:dxcore_interface.IDXCoreAdapterList.IsAdapterPreferenceSupported
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determines whether a specified [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference) value is understood by the OS.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,IsAdapterPreferenceSupported method, IDXCoreAdapterFactory.IsAdapterPreferenceSupported, IDXCoreAdapterFactory::IsAdapterPreferenceSupported, IsAdapterPreferenceSupported, IsAdapterPreferenceSupported method, IsAdapterPreferenceSupported method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::IsAdapterPreferenceSupported, dxcore_interface.idxcoreadapterfactory_isadapterpreferencesupported
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
 - IDXCoreAdapterList::IsAdapterPreferenceSupported
---

## -description

Determines whether a specified [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference) value is understood by the current operating system (OS). You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort).

## -parameters

### -param preference

Type: **[DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference)**

A [DXCoreAdapterPreference](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference) value that will be checked to see whether it's supported by the OS.

## -returns

Type: **bool**

Returns `true` if the sort type is understood by the current OS. Otherwise, returns `false`.

## -see-also

[IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)