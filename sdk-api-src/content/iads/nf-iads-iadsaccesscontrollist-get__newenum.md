---
UID: NF:iads.IADsAccessControlList.get__NewEnum
title: IADsAccessControlList::get__NewEnum (iads.h)
description: The IADsAccessControlList::get__NewEnum method is used to obtain an enumerator object for the ACL to enumerate ACEs.
helpviewer_keywords: ["IADsAccessControlList interface [ADSI]","get__NewEnum method","IADsAccessControlList.get__NewEnum","IADsAccessControlList::get__NewEnum","_ds_iadsaccesscontrollist_get__newenum","adsi.iadsaccesscontrollist__get____newenum","adsi.iadsaccesscontrollist_get__newenum","get__NewEnum","get__NewEnum method [ADSI]","get__NewEnum method [ADSI]","IADsAccessControlList interface","iads/IADsAccessControlList::get__NewEnum"]
old-location: adsi\iadsaccesscontrollist_get__newenum.htm
tech.root: adsi
ms.assetid: 569f3bfa-3933-43b3-9d16-c3d4382cfa9f
ms.date: 12/05/2018
ms.keywords: IADsAccessControlList interface [ADSI],get__NewEnum method, IADsAccessControlList.get__NewEnum, IADsAccessControlList::get__NewEnum, _ds_iadsaccesscontrollist_get__newenum, adsi.iadsaccesscontrollist__get____newenum, adsi.iadsaccesscontrollist_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsAccessControlList interface, iads/IADsAccessControlList::get__NewEnum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsAccessControlList::get__NewEnum
 - iads/IADsAccessControlList::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsAccessControlList.get__NewEnum
---

# IADsAccessControlList::get__NewEnum


## -description

The <b>IADsAccessControlList::get__NewEnum</b> method is used to obtain an enumerator object for the ACL to enumerate ACEs.

## -parameters

### -param retval [out]

Pointer to pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface used to retrieve
      <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface on an enumerator object for the ACL.

## -returns

This method returns the standard return values, including <b>S_OK</b> and <b>E_FAIL</b>. For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

Be aware  that there are two underscores in <b>get__NewEnum</b>.


#### Examples

The following code example makes an implicit call to the <b>get__NewEnum</b> method in the execution of the <b>For Each</b> loop.


```vb
Dim Dacl As IADsAccessControlList
Dim ace As IADsAccessControlEntry

On Error GoTo Cleanup

' Get DACL. Code omitted.

' Display the trustees for each of the ACEs
For Each ace In Dacl 
    Debug.Print ace.trustee
Next ace

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set Dacl = Nothing
    Set ace = Nothing

```


The following code example shows how to enumerate ACEs using <b>IADsAccessControlList::get__NewEnum</b>.


```cpp
HRESULT ListTrustees(IADsAccessControlList *pACL)
{
    IEnumVARIANT *pEnum = NULL;
    LPUNKNOWN     pUnk = NULL;
    ULONG  lFetch = 0;
    BSTR    bstr = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IDispatch *pDisp = NULL;
    VARIANT var;
    HRESULT hr = S_OK;
    
    VariantInit(&var);
     
    hr = pACL->get__NewEnum(&pUnk);
    if (FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface( IID_IEnumVARIANT, (void**) &pEnum );
    pUnk->Release();
    if (FAILED(hr)){goto Cleanup;}
     
    hr = pEnum->Next( 1, &var, &lFetch );
    if (FAILED(hr)){goto Cleanup;}
     
    while( hr == S_OK )
    {
        if ( lFetch == 1 )
        {
            if ( VT_DISPATCH != V_VT(&var) )
            {
                goto Cleanup;
            }
            pDisp = V_DISPATCH(&var);
            /////////////////////////
            // Get the individual ACE
            /////////////////////////
            hr = pDisp->QueryInterface( IID_IADsAccessControlEntry,(void**)&pACE ); 
            if ( SUCCEEDED(hr) )
            {
                pACE->get_Trustee(&bstr);
                printf("\n %S:\n", bstr);
                //ACE manipulation here
                SysFreeString(bstr);
                pACE->Release();
            }
            pACE->Release();
            pDisp->Release();
            VariantClear(&var);
        }
        hr = pEnum->Next( 1, &var, &lFetch );
    }
    Cleanup:        
        if(pEnum) pEnum->Release();
        if(pUnk) pUnk->Release();
        if(bstr) SysFreeString(bstr);
        if(pACE) pACE->Release();
        VariantClear(&var);
        return hr;
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>