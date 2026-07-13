---
UID: NF:oleacc.AccessibleChildren
title: AccessibleChildren function (oleacc.h)
description: Retrieves the child ID or IDispatch of each child within an accessible container object.
helpviewer_keywords: ["AccessibleChildren","AccessibleChildren function [Windows Accessibility]","_msaa_AccessibleChildren","msaa.accessiblechildren","oleacc/AccessibleChildren","winauto.accessiblechildren"]
old-location: winauto\accessiblechildren.htm
tech.root: WinAuto
ms.assetid: dc9262d8-f57f-41f8-8945-d95f38d197e9
ms.date: 12/05/2018
ms.keywords: AccessibleChildren, AccessibleChildren function [Windows Accessibility], _msaa_AccessibleChildren, msaa.accessiblechildren, oleacc/AccessibleChildren, winauto.accessiblechildren
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
 - AccessibleChildren
 - oleacc/AccessibleChildren
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-oleacc-l1-1-2.dll
 - Oleacc.dll
api_name:
 - AccessibleChildren
---

# AccessibleChildren function


## -description

Retrieves the child ID or <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> of each child within an accessible container object.

## -parameters

### -param paccContainer [in]

Type: <b>IAccessible*</b>

Pointer to the container object's <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface.

### -param iChildStart [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Specifies the zero-based index of the first child that is retrieved. This parameter is an index, not a child ID, and it is usually is set to zero (0).

### -param cChildren [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Specifies the number of children to retrieve. To retrieve the current number of children, an application calls <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchildcount">IAccessible::get_accChildCount</a>.

### -param rgvarChildren [out]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

Pointer to an array of <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> structures that receives information about the container's children. If the <b>vt</b> member of an array element is VT_I4, then the <b>lVal</b> member for that element is the child ID. If the <b>vt</b> member of an array element is VT_DISPATCH, then the <b>pdispVal</b> member for that element is the address of the child object's <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface.

### -param pcObtained [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

Address of a variable that receives the number of elements in the <i>rgvarChildren</i> array that is populated by the <b>AccessibleChildren</b> function. This value is the same as that of the <i>cChildren</i> parameter; however, if you request more children than exist, this value will be less than that of <i>cChildren</i>.

## -returns

Type: <b>STDAPI</b>

If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

<table>
<tr>
<th>Return code</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded, but there are fewer elements in the <i>rgvarChildren</i> array than there are children requested in <i>cChildren</i>.

</td>
</tr>
</table>

## -remarks

To retrieve information about all of the children in a container, the <i>iChildStart</i> parameter  must be zero (0), and <i>cChildren</i> must be the value returned by <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchildcount">IAccessible::get_accChildCount</a>.

When calling this function to obtain information about the children of a user interface element, it is recommended that clients obtain information about all of the children. For example, <i>iChildStart</i> must be zero (0), and <i>cChildren</i> must be the value returned by <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchildcount">IAccessible::get_accChildCount</a>.

If a child ID is returned for an element, then the container must provide information about the child element. To obtain information about the element, clients use the container's  <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer and specify the obtained child ID in calls to the <b>IAccessible</b> properties.

Clients must call the <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method for any <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interfaces retrieved by this function, and free the array when it is no longer required.


#### Examples

The following example function displays a view of the element tree below the element that is passed in. The name and role of each element are printed by user-defined functions that are not shown here.




```

HRESULT WalkTreeWithAccessibleChildren(IAccessible* pAcc, int depth)
{
    HRESULT hr;
    long childCount;
    long returnCount;

    if (!pAcc)
    {
        return E_INVALIDARG;
    }
    hr = pAcc->get_accChildCount(&childCount);
    if (FAILED(hr))
    {
        return hr;
    };
    if (childCount == 0)
    {
        return S_FALSE;
    }
    VARIANT* pArray = new VARIANT[childCount];
    hr = AccessibleChildren(pAcc, 0L, childCount, pArray, &returnCount);
    if (FAILED(hr))
    {
        return hr;
    };

    // Iterate through children.
    for (int x = 0; x < returnCount; x++)
    {
        VARIANT vtChild = pArray[x];
        // If it's an accessible object, get the IAccessible, and recurse.
        if (vtChild.vt == VT_DISPATCH)
        {
            IDispatch* pDisp = vtChild.pdispVal;
            IAccessible* pChild = NULL;
            hr = pDisp->QueryInterface(IID_IAccessible, (void**) &pChild);
            if (hr == S_OK)
            {
                for (int y = 0; y < depth; y++)
                {
                    printf("  ");
                }
                PrintName(pChild, CHILDID_SELF);
                printf("(Object) ");
                PrintRole(pChild, CHILDID_SELF);
                WalkTreeWithAccessibleChildren(pChild, depth + 1);
                pChild->Release();
            }
            pDisp->Release();
        }
        // Else it's a child element so we have to call accNavigate on the parent,
        //   and we do not recurse because child elements can't have children.
        else
        {
            for (int y = 0; y < depth; y++)
            {
                printf("  ");
            }
            PrintName(pAcc, vtChild.lVal);
            printf("(Child element) ");
            PrintRole(pAcc, vtChild.lVal);
        }
    }
    delete[] pArray;
    return S_OK;
}

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>