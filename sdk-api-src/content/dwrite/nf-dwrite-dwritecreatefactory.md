---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
if (SUCCEEDED(hr))
{
    hr = DWriteCreateFactory(
        DWRITE_FACTORY_TYPE_SHARED,
        __uuidof(IDWriteFactory),
        reinterpret_cast&lt;IUnknown**&gt;(&amp;pDWriteFactory_)
        );
}

</pre>
</td>
</tr>
</table></span></div>


