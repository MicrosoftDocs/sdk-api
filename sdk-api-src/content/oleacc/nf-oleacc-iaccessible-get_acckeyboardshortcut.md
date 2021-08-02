---
UID: NF:oleacc.IAccessible.get_accKeyboardShortcut
title: IAccessible::get_accKeyboardShortcut (oleacc.h)
description: The IAccessible::get_accKeyboardShortcut method retrieves the specified object's shortcut key or access key, also known as the mnemonic. All objects that have a shortcut key or an access key support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accKeyboardShortcut method","IAccessible.get_accKeyboardShortcut","IAccessible::get_accKeyboardShortcut","_msaa_IAccessible_get_accKeyboardShortcut","get_accKeyboardShortcut","get_accKeyboardShortcut method [Windows Accessibility]","get_accKeyboardShortcut method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_acckeyboardshortcut","oleacc/IAccessible::get_accKeyboardShortcut","winauto.iaccessible_iaccessible__get_acckeyboardshortcut"]
old-location: winauto\iaccessible_iaccessible__get_acckeyboardshortcut.htm
tech.root: WinAuto
ms.assetid: 0d91c791-1e9b-45da-8fa6-b879ac6d11a7
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accKeyboardShortcut method, IAccessible.get_accKeyboardShortcut, IAccessible::get_accKeyboardShortcut, _msaa_IAccessible_get_accKeyboardShortcut, get_accKeyboardShortcut, get_accKeyboardShortcut method [Windows Accessibility], get_accKeyboardShortcut method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_acckeyboardshortcut, oleacc/IAccessible::get_accKeyboardShortcut, winauto.iaccessible_iaccessible__get_acckeyboardshortcut
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - IAccessible::get_accKeyboardShortcut
 - oleacc/IAccessible::get_accKeyboardShortcut
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accKeyboardShortcut
---

# IAccessible::get_accKeyboardShortcut


## -description

The <b>IAccessible::get_accKeyboardShortcut</b> method retrieves the specified object's shortcut key or access key, also known as the mnemonic. All objects that have a shortcut key or an access key support this property.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved keyboard shortcut belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pszKeyboardShortcut [out, retval]

Type: <b>BSTR*</b>

 Address of a <b>BSTR</b> that receives a localized string that identifies the keyboard shortcut, or <b>NULL</b> if no keyboard shortcut is associated with the specified object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="/windows/desktop/WinAuto/checking-iaccessible-return-values">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object does not have an associated keyboard shortcut.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this property.

</td>
</tr>
</table>

## -remarks

An access key is an underlined character in the text of a menu, menu item, or label of a button or some other control. For example, a user can display a menu by pressing the ALT key while also pressing the indicated underlined key, such as ALT+F to open the <u>F</u>ile menu. To use the access key of a menu item, the menu that contains the item must be active.

Controls such as toolbar buttons and menu items often have an associated shortcut key, also known as a keyboard accelerator. Some menu items may have both an access key and a shortcut key, and some may have only one. For example, a menu item called <u>N</u>ew has an access key N and a shortcut key CTRL+N. The menu does not have to be active for the shortcut key to work.

<b>Note to client developers:  </b><p class="note">If this property returns a single character, you cannot assume it is an access key or a keyboard shortcut. With standard menu items, the access key is returned by <b>IAccessible::get_accKeyboardShortcut</b>, and the shortcut key is returned as part of the menu item name returned from <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accname">IAccessible::get_accName</a>. In general, access keys tend to be defined as ALT + &lt;letter&gt;, and keyboard shortcuts tend to be CTRL + &lt;letter&gt;.



<b>Note to server developers:  </b>If the UI element can receive keyboard focus, then you should expose the access key for the element. If the UI element cannot receive keyboard focus (such as toolbar icons), then you should display the shortcut key.

Because shortcut keys are usually determined by the application rather than by the control itself, servers can usually return the value obtained from the standard accessible object for the window.



<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function retrieves the keyboard shortcut for the specified accessible object, or one of its children, and prints it to the console.


```cpp

HRESULT PrintShortcut(IAccessible* pAcc, long child)
{
    if (pAcc == NULL)
    {
        return E_INVALIDARG;
    }
    BSTR bstrShortcut;
    VARIANT varObj;
    varObj.vt = VT_I4;
    varObj.lVal = child;
    HRESULT hr = pAcc->get_accKeyboardShortcut(varObj, &bstrShortcut);
    if (hr == S_OK)
    {
        printf("Shortcut: %S\n", bstrShortcut);
        SysFreeString(bstrShortcut);
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accname">IAccessible::get_accName</a>



<a href="/windows/desktop/WinAuto/keyboardshortcut-property">KeyboardShortcut Property</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>
