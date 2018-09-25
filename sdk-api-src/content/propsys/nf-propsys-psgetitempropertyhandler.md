---
UID: NF:propsys.PSGetItemPropertyHandler
title: PSGetItemPropertyHandler function
author: windows-sdk-content
description: Retrieves a property handler for a Shell item.
old-location: properties\PSGetItemPropertyHandler.htm
tech.root: properties
ms.assetid: 7b7fd260-c863-41f7-8594-4ee435090228
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: PSGetItemPropertyHandler, PSGetItemPropertyHandler function [Windows Properties], _shell_PSGetItemPropertyHandler, properties.PSGetItemPropertyHandler, propsys/PSGetItemPropertyHandler, shell.PSGetItemPropertyHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetItemPropertyHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PSGetItemPropertyHandler function


## -description


Retrieves a property handler for a Shell item.


## -parameters




### -param punkItem [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a Shell item that supports <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.

                    

<b>Windows XP:</b> Use <a href="https://msdn.microsoft.com/d4371cdf-a8f4-4a39-ba66-97fd40ed46ae">SHCreateShellItem</a> to create the Shell item.

<b>Windows Vista:</b> Use <a href="https://msdn.microsoft.com/a6dcddd9-cdbc-4cf9-97e3-d1b562283344">SHCreateItemFromIDList</a>, <a href="https://msdn.microsoft.com/81e48318-b6a4-4b1a-8b78-21c00b9dc485">SHCreateItemFromParsingName</a>, <a href="https://msdn.microsoft.com/af6c2e8b-c812-4858-a9db-24549dedc2aa">SHCreateItemFromRelativeName</a>, <a href="https://msdn.microsoft.com/dc75ee60-7319-4a11-949e-dd0c3deabd8f">SHCreateItemInKnownFolder</a>, or <a href="https://msdn.microsoft.com/8fb84a20-d8f2-4c7c-bfb1-a22791b8636a">SHCreateItemWithParent</a> to create the Shell item.


### -param fReadWrite [in]

Type: <b>BOOL</b>

<b>TRUE</b> to retrieve a read/write property handler. <b>FALSE</b> to retrieve a read-only property handler.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID of the interface the handler object should return. This should be <a href="shell.IPropertyStore">IPropertyStore</a> or an interface derived from <b>IPropertyStore</b>.


### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This function is supported in Windows XP and Windows Vista. For applications supported only on Windows Vista or later, it is recommended that you use <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> instead of <a href="shell.PSGetItemPropertyHandler">PSGetItemPropertyHandler</a>. That method provides a richer set of properties in the property store that is returned.

This function is approximately equivalent to passing the GPS_HANDLERPROPERTIESONLY flag to <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>.

You must initialize Component Object Model (COM) with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="shell.PSGetItemPropertyHandler">PSGetItemPropertyHandler</a>. COM must remain initialized for the lifetime of this object.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetItemPropertyHandler">PSGetItemPropertyHandler</a> to obtain a property handler for an item.


```cpp
// IShellItem *psi;
// Assume variable psi is valid and initialized.
IPropertyStore *pStore;

HRESULT hr = PSGetItemPropertyHandler(psi, FALSE, IID_PPV_ARGS(&pStore));

if (SUCCEEDED(hr))
{
    // pStore is now valid and contains properties exposed through the 
    // property handler for the item.
 
    pStore->Release();
}
```




