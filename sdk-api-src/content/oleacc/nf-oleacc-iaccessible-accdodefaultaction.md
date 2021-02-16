---
UID: NF:oleacc.IAccessible.accDoDefaultAction
title: IAccessible::accDoDefaultAction (oleacc.h)
description: The IAccessible::accDoDefaultAction method performs the specified object's default action. Not all objects have a default action.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","accDoDefaultAction method","IAccessible.accDoDefaultAction","IAccessible::accDoDefaultAction","_msaa_IAccessible_accDoDefaultAction","accDoDefaultAction","accDoDefaultAction method [Windows Accessibility]","accDoDefaultAction method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__accdodefaultaction","oleacc/IAccessible::accDoDefaultAction","winauto.iaccessible_iaccessible__accdodefaultaction"]
old-location: winauto\iaccessible_iaccessible__accdodefaultaction.htm
tech.root: WinAuto
ms.assetid: 5b731f52-d0b0-4b69-91a0-fdd84e91533d
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],accDoDefaultAction method, IAccessible.accDoDefaultAction, IAccessible::accDoDefaultAction, _msaa_IAccessible_accDoDefaultAction, accDoDefaultAction, accDoDefaultAction method [Windows Accessibility], accDoDefaultAction method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__accdodefaultaction, oleacc/IAccessible::accDoDefaultAction, winauto.iaccessible_iaccessible__accdodefaultaction
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
req.redist: Active Accessibility 1.3 RDK on Windows NT Server 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - IAccessible::accDoDefaultAction
 - oleacc/IAccessible::accDoDefaultAction
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
 - IAccessible.accDoDefaultAction
---

# IAccessible::accDoDefaultAction


## -description

The <b>IAccessible::accDoDefaultAction</b> method performs the specified object's default action. Not all objects have a default action.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the default action belongs to the object or one of the object's child elements. For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the method. This value is returned for controls that do not perform actions, such as edit fields.

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
</table>

## -remarks

Clients retrieve a string that describes the object's default action by calling <b>IAccessible::get_accDefaultAction</b>.

<b>Note to client developers:  </b>When used on a menu item in a standard system menu, <b>accDoDefaultAction</b> returns S_OK but fails to perform the action if the character used in the access key (the underlined character in the text of a menu item name, also called a mnemonic) is ?, !, @, or any other character that requires the SHIFT key or another modifier key. This also happens on international keyboards with an access key character that requires the ALT GR key to be pressed. This is not an issue for menus in other applications, such as Microsoft Office or Windows Internet Explorer. For more information about access keys, see <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut">IAccessible::get_accKeyboardShortcut</a>.

Also, while <b>accDoDefaultAction</b> is supposed to return immediately, some implementations block the return. For example, if clicking a link displays a dialog, some implementations will block the return until the dialog is dismissed. Such delays can prevent client applications from processing a dialog box. Servers should avoid implementations that block returns.



<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example shows a possible implementation for a custom list control whose default action is a double-click a child item. To prevent blocking, the method posts a custom message that, when received by the control window, triggers an action, such as displaying item properties.


```cpp

// Assume a previous definition such as this: 
// #define CUSTOMLB_DEFERDOUBLECLICK   (WM_USER + 1) 

HRESULT STDMETHODCALLTYPE AccServer::accDoDefaultAction( 
    VARIANT varChild) 
{
    if (varChild.vt != VT_I4)
    {
        return E_INVALIDARG;
    }
    if (varChild.lVal != CHILDID_SELF)
    {
        // It is assumed that the control does its own checking to see which 
        // item has the focus when it receives this message.
        PostMessage(m_hwnd, CUSTOMLB_DEFERDOUBLECLICK, 0, 0);
    }
    return S_OK;
};

```


<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function performs the default action on a control.


```cpp

HRESULT DoAction(IAccessible* pAcc)
{
        VARIANT varId;
        varId.vt = VT_I4;
        varId.lVal = CHILDID_SELF;
        return pAcc->accDoDefaultAction(varId);
}

```

## -see-also

<a href="/windows/desktop/WinAuto/appendix-a--supported-user-interface-elements-reference">Appendix A: Supported User Interface Elements Reference</a>



<a href="/windows/desktop/WinAuto/defaultaction-property">DefaultAction Property</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accdefaultaction">IAccessible::get_accDefaultAction</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut">IAccessible::get_accKeyboardShortcut</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>