---
UID: NF:propsys.PSGetItemPropertyHandlerWithCreateObject
title: PSGetItemPropertyHandlerWithCreateObject function
author: windows-driver-content
description: Retrieves a property handler for a Shell item.
old-location: properties\PSGetItemPropertyHandlerWithCreateObject.htm
old-project: properties
ms.assetid: 82e0aa15-b67c-4c0a-bafb-f1dc5f822aec
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: PSGetItemPropertyHandlerWithCreateObject, PSGetItemPropertyHandlerWithCreateObject function [Windows Properties], _shell_PSGetItemPropertyHandlerWithCreateObject, properties.PSGetItemPropertyHandlerWithCreateObject, propsys/PSGetItemPropertyHandlerWithCreateObject, shell.PSGetItemPropertyHandlerWithCreateObject
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSGetItemPropertyHandlerWithCreateObject
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSGetItemPropertyHandlerWithCreateObject function


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


### -param punkCreateObject [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a class factory object that supports <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param ppv [out]

Type: <b>void**</b>

When this function returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> or <a href="shell.IPropertyStoreCapabilities">IPropertyStoreCapabilities</a>.


## -returns



Type: <b>PSSTDAPI</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This function is supported in Windows XP as part of the Microsoft Windows Desktop Search (WDS) redistributable which includes <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> and supporting interfaces. For applications supported only on Windows Vista or later, we recommend that you use <a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">IShellItem2::GetPropertyStoreWithCreateObject</a> instead of <a href="shell.PSGetItemPropertyHandlerWithCreateObject">PSGetItemPropertyHandlerWithCreateObject</a> because <b>IShellItem2::GetPropertyStoreWithCreateObject</b> provides a richer set of properties in the property store that is returned.

This function is approximately equivalent to passing the GPS_HANDLERPROPERTIESONLY flag to <a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">IShellItem2::GetPropertyStoreWithCreateObject</a>.

The <i>punkCreateObject</i> parameter enables the creation of a property store in a different context than that of the caller. For instance, the <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> implementation can cause the property store to be created in another process. This parameter is used only for property handlers that support it and that are registered under 

                
                   <b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>Windows</b>\<b>CurrentVersion</b>\<b>PropertySystem</b>\<b>PropertyHandlers</b>

You must initialize Component Object Model (COM) with <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before you call <a href="shell.PSGetItemPropertyHandlerWithCreateObject">PSGetItemPropertyHandlerWithCreateObject</a>. COM must remain initialized for the lifetime of this object.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetItemPropertyHandlerWithCreateObject">PSGetItemPropertyHandlerWithCreateObject</a> to obtain a property handler for an item.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IShellItem *psi;
// ICreateObject *pco;
// Assume variables pco and psi are valid and initialized.
IPropertyStore *pStore;

HRESULT hr = PSGetItemPropertyHandlerWithCreateObject(psi, FALSE, pco, IID_PPV_ARGS(&amp;pStore));

if (SUCCEEDED(hr))
{
    // pStore is now valid and contains properties exposed through the 
    // property handler for the item.
 
    pStore-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">IShellItem2::GetPropertyStoreWithCreateObject</a>



<a href="shell.Building_Property_Handlers_Property_Handlers">Initializing Property Handlers</a>
 

 

