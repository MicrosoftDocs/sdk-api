---
UID: NF:dwrite.DWriteCreateFactory
title: DWriteCreateFactory function
author: windows-sdk-content
description: Creates a DirectWrite factory object that is used for subsequent creation of individual DirectWrite objects.
old-location: directwrite\dwritecreatefactory.htm
tech.root: DirectWrite
ms.assetid: c74c0906-0a5c-4ab8-87cf-a195566e1d9e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DWriteCreateFactory, DWriteCreateFactory function [Direct Write], directwrite.dwritecreatefactory, dwrite/DWriteCreateFactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dwrite.dll
api_name:
 - DWriteCreateFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWriteCreateFactory function


## -description


Creates a DirectWrite factory object that is used for subsequent creation of individual DirectWrite objects.


## -parameters




### -param factoryType [in]

Type: <b><a href="https://msdn.microsoft.com/ce51d8cd-3125-49e3-878c-9d4b446e2422">DWRITE_FACTORY_TYPE</a></b>

A value that specifies whether the factory object will be shared or isolated.


### -param iid [in]

Type: <b>REFIID</b>

A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>).


### -param factory [out]

Type: <b>IUnknown**</b>

An address of a pointer to the newly created DirectWrite factory object.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> factory object that is used for subsequent creation of individual DirectWrite objects.
 DirectWrite factory contains internal state data such as font loader registration and cached font data.
 In most cases it is recommended you use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state data, and thereby reduce memory usage.
 However, there are cases when it is desirable to reduce the impact of a component,
 such as a plug-in from an untrusted source, on the rest of the process, by sandboxing and isolating it from the rest of the process components. In such cases, it is recommended you use an isolated factory for the sandboxed component.

The following example shows how to create a shared <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> factory.


```cpp

if (SUCCEEDED(hr))
{
    hr = DWriteCreateFactory(
        DWRITE_FACTORY_TYPE_SHARED,
        __uuidof(IDWriteFactory),
        reinterpret_cast<IUnknown**>(&pDWriteFactory_)
        );
}


```




