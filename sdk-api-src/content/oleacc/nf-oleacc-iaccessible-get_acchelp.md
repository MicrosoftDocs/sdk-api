---
UID: NF:oleacc.IAccessible.get_accHelp
title: IAccessible::get_accHelp (oleacc.h)
description: The IAccessible::get_accHelp method retrieves the Help property string of an object. Not all objects support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accHelp method","IAccessible.get_accHelp","IAccessible::get_accHelp","_msaa_IAccessible_get_accHelp","get_accHelp","get_accHelp method [Windows Accessibility]","get_accHelp method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_acchelp","oleacc/IAccessible::get_accHelp","winauto.iaccessible_iaccessible__get_acchelp"]
old-location: winauto\iaccessible_iaccessible__get_acchelp.htm
tech.root: WinAuto
ms.assetid: ef541ef9-ae9f-4a8c-8dd1-f221eddb55c7
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accHelp method, IAccessible.get_accHelp, IAccessible::get_accHelp, _msaa_IAccessible_get_accHelp, get_accHelp, get_accHelp method [Windows Accessibility], get_accHelp method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_acchelp, oleacc/IAccessible::get_accHelp, winauto.iaccessible_iaccessible__get_acchelp
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
 - IAccessible::get_accHelp
 - oleacc/IAccessible::get_accHelp
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
 - IAccessible.get_accHelp
---

# IAccessible::get_accHelp


## -description

The <b>IAccessible::get_accHelp</b> method retrieves the <b>Help</b> property string of an object. Not all objects support this property.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved help information belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about one of the object's child elements). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pszHelp [out, retval]

Type: <b>BSTR*</b>

Address of a <b>BSTR</b> that receives the localized string containing the help information for the specified object, or <b>NULL</b> if no help information is available.

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
No help information is available.

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

None of the predefined and common controls support this property.

<b>Note to server developers:  </b>Localize the string returned from this property.

This property returns a string, whereas <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acchelptopic">IAccessible::get_accHelpTopic</a> provides access to a Help topic in <a href="/windows/win32/api/winuser/nf-winuser-winhelpa">WinHelp</a>. Objects are not required to support both <b>IAccessible::get_accHelp</b> and <b>IAccessible::get_accHelpTopic</b>, but they must support at least one. If they easily return a string, they must support <b>IAccessible::get_accHelp</b> ; otherwise they must support <b>IAccessible::get_accHelpTopic</b>. If both are supported, <b>IAccessible::get_accHelpTopic</b> provides more detailed information.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows one possible implementation of this method for a custom list box. Different text is displayed depending on the status of the contact in the list. For simplicity, the example does not localize the returned string.


```cpp

// m_pControl is the custom control that returns this accessible object. 
// 'online' is an enumerated value. 

HRESULT STDMETHODCALLTYPE AccServer::get_accHelp( 
    VARIANT varChild,
    BSTR *pszHelp)
{
    *pszHelp = NULL;
    if (varChild.vt != VT_I4)
    {
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        *pszHelp = SysAllocString(L"Contact list.");
    }
    else
    {
        int index = (int)varChild.lVal - 1;
        CustomListControlItem* pItem = m_pControl->GetItemAt(index);
        if (pItem == NULL)
        {
            return E_INVALIDARG;
        }
        if (pItem->GetStatus() == online)
        {
            *pszHelp = SysAllocString(L"Online contact.");
        }
        else 
        {
            *pszHelp = SysAllocString(L"Offline contact.");
        }
    }
    return S_OK;
};

```

## -see-also

<a href="/windows/desktop/WinAuto/help-property">Help Property</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accdescription">IAccessible::get_accDescription</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acchelptopic">IAccessible::get_accHelpTopic</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>
