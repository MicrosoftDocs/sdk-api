---
UID: NN:iads.IADsContainer
title: IADsContainer (iads.h)
description: The IADsContainer interface enables an ADSI container object to create, delete, and manage contained ADSI objects. Container objects represent hierarchical directory trees, such as in a file system, and to organize the directory hierarchy.
helpviewer_keywords: ["IADsContainer","IADsContainer interface [ADSI]","IADsContainer interface [ADSI]","described","_ds_iadscontainer","adsi.iadscontainer","iads/IADsContainer"]
old-location: adsi\iadscontainer.htm
tech.root: adsi
ms.assetid: 6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2
ms.date: 12/05/2018
ms.keywords: IADsContainer, IADsContainer interface [ADSI], IADsContainer interface [ADSI],described, _ds_iadscontainer, adsi.iadscontainer, iads/IADsContainer
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
 - IADsContainer
 - iads/IADsContainer
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
 - IADsContainer
---

# IADsContainer interface


## -description

The <b>IADsContainer</b> interface enables an ADSI container 
    object to create, delete, and manage contained ADSI objects. Container objects represent hierarchical directory 
    trees, such as in a file system, and to organize the directory hierarchy.

You can use the <b>IADsContainer</b> interface to either 
    enumerate contained objects or manage their lifecycle. An example would be to recursively navigate a directory 
    tree. By querying the <b>IADsContainer</b> interface on an ADSI 
    object, you can determine if the object has any children. If the interface is not supported, the object is a leaf. 
    Otherwise, it is a container. You can continue this process for the newly found container objects. To create, 
    copy, or delete an object, send the request to the container object to perform the task.

## -inheritance

The <b>IADsContainer</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsContainer</b> also has these types of members:

## -remarks

To determine if an object is a container, use the <a href="/windows/desktop/ADSI/iadsclass-property-methods">IADsClass.Container</a> property of the object.

When you bind to a container object using its GUID (or SID), you can only perform specific operations on the container object. These operations include examination of the object attributes and enumeration of the object's immediate children. These operations are shown in the following code example.


```vb
Dim con As IADsContainer
Dim obj As IADs
Set con = GetObject("LDAP://svr01/<GUID=xxxx>")
con.Filter = Array("user")
For Each item In con
    debug.print item.Name " &  " of " & item.Class
Next
```


All other operations, that is, <b>GetObject</b>, <b>Create</b>, <b>Delete</b>, <b>CopyHere</b>, and <b>MoveHere</b> are not supported in the container's GUID representation. For example, the last line of the following code example will result in an error.


```vb
Dim con As IADsContainer
Dim obj As IADs
Set con = GetObject("LDAP://svr01/<GUID=xxxx>")
Set obj = con.GetObject("user", "CN=Jeff Smith")
```


Binding, using GUID (or SID), is intended for low overhead and, thus, fast binds, which are often used for object introspection.

To call these methods of the container bound with its GUID (or SID), rebind to the object using its distinguished name.


```vb
Dim conGUID, conDN As IADsContainer
Dim obj As IADs
Set conGUID = GetObject("LDAP://svr/<GUID=xxxx>")
Set conDN=GetObject("LDAP://svr/" & conGUID.Get("distinguishedName"))
Set obj = conDN.GetObject("user", "CN=Jeff Smith")
```


For more information about object GUID representation, see <a href="/windows/desktop/ADSI/iads-property-methods">IADs.GUID</a>.


#### Examples

The following code example determines if an ADSI object is a container.


```vb
Dim obj As IADs
Dim cls As IADsClass
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(obj.Schema)
If (cls.Container = TRUE) Then
    MsgBox "The object is a container."
Else
    MsgBox "The object is a leaf."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cls = Nothing
```


The following code example determines if an ADSI object is a container.


```cpp
IADs *pADs = NULL;
IADsClass *pCls = NULL;
HRESULT hr = S_OK;
BSTR bstr;

hr = ADsGetObject(L"WinNT://myComputer,computer", IID_IADs, (void**)&pADs);
if(FAILED(hr)){return;}

pADs->get_Schema(&bstr);
hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
pADs->Release();
SysFreeString(bstr);

if(FAILED(hr)){return;}

VARIANT_BOOL isContainer;
pCls->get_Container(&isContainer);

if(isContainer) 
    printf("Object is a container.\n");
else
    printf("Object is not a container.\n");

pCls->Release();

```

## -see-also

<a href="/windows/desktop/ADSI/creating-and-deleting-objects">Creating and Deleting Objects</a>



<a href="/windows/desktop/ADSI/iads-property-methods">IADs::get_GUID</a>



<a href="/windows/desktop/ADSI/iadsclass-property-methods">IADsClass::get_Container</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnamespaces">IADsNamespaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
