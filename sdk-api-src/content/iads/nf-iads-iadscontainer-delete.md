---
UID: NF:iads.IADsContainer.Delete
title: IADsContainer::Delete (iads.h)
description: Deletes a specified directory object from this container.
helpviewer_keywords: ["Delete","Delete method [ADSI]","Delete method [ADSI]","IADsContainer interface","IADsContainer interface [ADSI]","Delete method","IADsContainer.Delete","IADsContainer::Delete","_ds_iadscontainer_delete","adsi.iadscontainer__delete","adsi.iadscontainer_delete","iads/IADsContainer::Delete"]
old-location: adsi\iadscontainer_delete.htm
tech.root: adsi
ms.assetid: 2f3873e0-376e-4212-a28d-bd9bc112f6cf
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [ADSI], Delete method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],Delete method, IADsContainer.Delete, IADsContainer::Delete, _ds_iadscontainer_delete, adsi.iadscontainer__delete, adsi.iadscontainer_delete, iads/IADsContainer::Delete
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
 - IADsContainer::Delete
 - iads/IADsContainer::Delete
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
 - IADsContainer.Delete
---

# IADsContainer::Delete


## -description

The <b>IADsContainer::Delete</b> method deletes a specified directory object from this container.

## -parameters

### -param bstrClassName [in]

The schema class object to delete. The name is that returned from the  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs::get_Class</a> method. Also, <b>NULL</b> is a valid option for this parameter.   Providing <b>NULL</b> for this parameter is the only way to deal with defunct schema classes. If an instance was created before the class became defunct, the only way to  delete the instance of the defunct class is to call <b>IADsContainer::Delete</b> and provide <b>NULL</b> for this parameter.

### -param bstrRelativeName [in]

Name of the object as it is known in the underlying directory and identical to the name retrieved with the  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs::get_Name</a> method.

## -returns

This method supports the standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The object to be deleted must be a leaf object or a childless subcontainer. To delete a container and its children, that is, a subtree, use  <a href="/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a>.

The specified object is immediately removed after calling  <b>IADsContainer::Delete</b> and calling  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> on the container object is unnecessary.

When using the  <b>IADsContainer::Delete</b> method to delete an object in C/C++ applications, release the interface pointers to that object as well. This is because the method removes the object from the underlying directory immediately, but leave intact any interface pointers held, in memory, by the application, for the deleted object. If not released, confusion can occur in that you may call  <a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a> and  <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a> on the deleted object without error, but will receive an error when you call  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> or  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> on the deleted object.


#### Examples

The following code example deletes a user object from the container in Active Directory.


```vb
Dim cont as IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
cont.Delete "user", "CN=JeffSmith"

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing

```


The following code example deletes a user object from the container under WinNT provider.


```vb
Dim cont as IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("WinNT://Fabrikam")
cont.Delete "user", "jeffsmith"

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
```


The following code example deletes a user using  <b>IADsContainer::Delete</b>.


```cpp
HRESULT hr = S_OK;
IADsContainer *pCont=NULL;
 
CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine", 
                  IID_IADsContainer, 
                  (void**) &pCont);
if ( !SUCCEEDED(hr) )
{
     return hr;
}
 
hr = pCont->Delete(CComBSTR("user"), CComBSTR("JeffSmith"));
pCont->Release();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error
  Codes</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-get">IADs::Get</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs::Put</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-iads">IADs::get_Class</a>



<b>IADs::get_Name</b>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-create">IADsContainer::Create</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a>