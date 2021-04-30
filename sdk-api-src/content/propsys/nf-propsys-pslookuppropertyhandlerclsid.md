---
UID: NF:propsys.PSLookupPropertyHandlerCLSID
title: PSLookupPropertyHandlerCLSID function (propsys.h)
description: Gets the class identifier (CLSID) of a per-computer, registered file property handler.
helpviewer_keywords: ["PSLookupPropertyHandlerCLSID","PSLookupPropertyHandlerCLSID function [Windows Properties]","_shell_PSLookupPropertyHandlerCLSID","properties.PSLookupPropertyHandlerCLSID","propsys/PSLookupPropertyHandlerCLSID","shell.PSLookupPropertyHandlerCLSID"]
old-location: properties\PSLookupPropertyHandlerCLSID.htm
tech.root: properties
ms.assetid: 43f90a33-9bd6-4e47-ab92-5e0d01ba268a
ms.date: 12/05/2018
ms.keywords: PSLookupPropertyHandlerCLSID, PSLookupPropertyHandlerCLSID function [Windows Properties], _shell_PSLookupPropertyHandlerCLSID, properties.PSLookupPropertyHandlerCLSID, propsys/PSLookupPropertyHandlerCLSID, shell.PSLookupPropertyHandlerCLSID
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSLookupPropertyHandlerCLSID
 - propsys/PSLookupPropertyHandlerCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSLookupPropertyHandlerCLSID
---

# PSLookupPropertyHandlerCLSID function


## -description

Gets the class identifier (CLSID) of a per-computer, registered file property handler.

## -parameters

### -param pszFilePath [in]

Type: <b>PCWSTR</b>

Pointer to a null-terminated, Unicode buffer that contains the absolute path of the file whose property handler CLSID is requested.

### -param pclsid [out]

Type: <b>CLSID*</b>

When this function returns, contains the requested property handler CLSID.

## -returns

Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

For information on how to register your handler, see <a href="/windows/desktop/properties/building-property-handlers-property-handlers">Initializing Property Handlers</a>.

This function returns only those handlers registered under <b>HKEY_LOCAL_MACHINE</b>.

Most calling applications should not need to call this method or use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create a property handler directly. Instead, calling applications should use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a> to create a property store for a Shell item on Windows Vista. <b>IShellItem2::GetPropertyStore</b> provides the largest set of available properties for a Shell item, and the most options for customizing exactly which properties to return.

If no property handler is registered for the specified file, this function returns an error code. When this happens, it might still be possible to read certain file system properties from the property store returned from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>.

Applications that need to create a property handler from code and that must run both on Windows Vista and on Windows XP can call <a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandler">PSGetItemPropertyHandler</a> to create a property store for a Shell item through the Microsoft Windows Desktop Search (WDS) redistributable.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-pslookuppropertyhandlerclsid">PSLookupPropertyHandlerCLSID</a>.


```cpp
CLSID clsid;

HRESULT hr = PSLookupPropertyHandlerCLSID(L"C:\\windows\\system32\\shell32.dll", &clsid);

if (SUCCEEDED(hr))
{
    // clsid contains the CLSID of the property handler used for 
    // C:\windows\system32\shell32.dll.
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore">IShellItem2::GetPropertyStore</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetitempropertyhandler">PSGetItemPropertyHandler</a>