---
UID: NF:oleacc.IAccessible.get_accRole
title: IAccessible::get_accRole (oleacc.h)
description: The IAccessible::get_accRole method retrieves information that describes the role of the specified object. All objects support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accRole method","IAccessible.get_accRole","IAccessible::get_accRole","_msaa_IAccessible_get_accRole","get_accRole","get_accRole method [Windows Accessibility]","get_accRole method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accrole","oleacc/IAccessible::get_accRole","winauto.iaccessible_iaccessible__get_accrole"]
old-location: winauto\iaccessible_iaccessible__get_accrole.htm
tech.root: WinAuto
ms.assetid: 38800c5e-12a5-4825-a4c4-825a159c67f1
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accRole method, IAccessible.get_accRole, IAccessible::get_accRole, _msaa_IAccessible_get_accRole, get_accRole, get_accRole method [Windows Accessibility], get_accRole method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accrole, oleacc/IAccessible::get_accRole, winauto.iaccessible_iaccessible__get_accrole
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
 - IAccessible::get_accRole
 - oleacc/IAccessible::get_accRole
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
 - IAccessible.get_accRole
---

# IAccessible::get_accRole


## -description

The <b>IAccessible::get_accRole</b> method retrieves information that describes the role of the specified object. All objects support this property.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved role information belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pvarRole [out, retval]

Type: <b>VARIANT*</b>

Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> that receives an <a href="/windows/desktop/WinAuto/object-roles">object role</a> constant. The <b>vt</b> member must be VT_I4. The <b>lVal</b> member receives an object role constant.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
</table>

## -remarks

Clients call <a href="/windows/desktop/api/oleacc/nf-oleacc-getroletexta">GetRoleText</a> to retrieve a localized string that describes the object's role.

<b>Note to server developers:  </b>You must use the predefined role constants.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code is a possible implementation of this method for a custom list box that maintains its own list items.


```cpp

HRESULT STDMETHODCALLTYPE AccServer::get_accRole( 
    VARIANT varChild,
    VARIANT *pvarRole)
{
    if (varChild.vt != VT_I4)
    {
        pvarRole->vt = VT_EMPTY;
        return E_INVALIDARG;
    }

    pvarRole->vt = VT_I4;

    if (varChild.lVal == CHILDID_SELF)
    {
        pvarRole->lVal = ROLE_SYSTEM_LIST;
    }
    else
    {
        pvarRole->lVal = ROLE_SYSTEM_LISTITEM;
    }
    return S_OK;
};

```


<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function displays the role of an accessible object or child element.


```cpp

HRESULT PrintRole(IAccessible* pAcc, long childId)
{
    DWORD roleId;
    if (pAcc == NULL)
    {
        return E_INVALIDARG;    
    }
    VARIANT varChild;
    varChild.vt = VT_I4;
    varChild.lVal = childId;
    VARIANT varResult;
    HRESULT hr = pAcc->get_accRole(varChild, &varResult);
    if ((hr == S_OK) && (varResult.vt == VT_I4))
    {
        roleId = varResult.lVal;
        UINT   roleLength;
        LPTSTR lpszRoleString;

        // Get the length of the string. 
        roleLength = GetRoleText(roleId, NULL, 0);

        // Allocate memory for the string. Add one character to 
        // the length you got in the previous call to make room 
        // for the null character. 
        lpszRoleString = (LPTSTR)malloc((roleLength+1) * sizeof(TCHAR));
        if (lpszRoleString != NULL)
        {
            // Get the string. 
            GetRoleText(roleId, lpszRoleString, roleLength + 1);
#ifdef UNICODE
            printf("Role: %S\n", lpszRoleString);
#else
            printf(("Role: %s\n", lpszRoleString);
#endif
            // Free the allocated memory 
            free(lpszRoleString);
        }
        else 
        {
            return E_OUTOFMEMORY;
        }
    }
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-getroletexta">GetRoleText</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/WinAuto/role-property">Role Property</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>