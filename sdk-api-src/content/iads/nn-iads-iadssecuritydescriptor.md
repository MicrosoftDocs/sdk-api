---
UID: NN:iads.IADsSecurityDescriptor
title: IADsSecurityDescriptor
author: windows-sdk-content
description: Provides access to properties on an ADSI security descriptor object.
old-location: adsi\iadssecuritydescriptor.htm
tech.root: ADSI
ms.assetid: c77547ab-e666-4d72-b8ef-4b2f3d61ad38
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ADsSecurityUtility, IADsSecurityDescriptor, IADsSecurityDescriptor interface [ADSI], IADsSecurityDescriptor interface [ADSI],described, _ds_iadssecuritydescriptor, adsi.iadssecuritydescriptor, iads/IADsSecurityDescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityDescriptor
 - ADsSecurityUtility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsSecurityDescriptor interface


## -description


The <b>IADsSecurityDescriptor</b> interface provides access to properties on an ADSI security descriptor object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityDescriptor</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsSecurityDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsSecurityDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe30a23a-ccf0-4852-bfcc-9f5a010bd0ec">CopySecurityDescriptor</a>
</td>
<td align="left" width="63%">
Copies the security descriptor.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsSecurityDescriptor</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">Control</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the Security_Descriptor_Control flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">DaclDefaulted</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag that indicates if the DACL is derived from a default mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">DiscretionaryAcl</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the discretionary ACL associated with the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">Group</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the group that owns the object associated with the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">GroupDefaulted</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag that indicates if the group data is derived by a default mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">Owner</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the owner of the object associated with the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">OwnerDefaulted</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag that indicates if the owner data is derived by a default mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">Revision</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the revision number assigned to the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">SaclDefaulted</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the flag that indicates if the SACL is derived from a default mechanism.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0c50740-de98-4913-b3df-6fd53263bcc8">SystemAcl</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the system ACL associated with the security descriptor.

</td>
</tr>
</table> 


## -remarks



Use this interface to examine and change the access controls to an Active Directory directory service object. You can also use it to create copies of a security descriptor. To get this interface, use the <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs.Get</a> method to obtain the <b>ntSecurityDescriptor</b> attribute of the object. For more information about how  to create  a new security descriptor and set it on an object, see <a href="https://msdn.microsoft.com/b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb">Creating a Security Descriptor for a New Directory Object</a> and <a href="https://msdn.microsoft.com/32b786d2-e676-4402-ad22-550de9289494">Null DACLs and Empty DACLs</a>.

Often, it is not possible to modify all portions of the security descriptor. For example, if the current user has full control of an object, but is not an administrator and does not own the object, the user can modify the DACL, but cannot modify the owner. This will cause an error when the <b>ntSecurityDescriptor</b> is updated. To avoid this problem, the <a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a> interface can be used to specify the specific portions of the security descriptor that should be modified.


#### Examples

The following code example shows how to use the <a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a> interface to only modify specific portions of the security descriptor.


```vb
Const ADS_OPTION_SECURITY_MASK = 3
Const ADS_SECURITY_INFO_OWNER = 1
Const ADS_SECURITY_INFO_GROUP = 2
Const ADS_SECURITY_INFO_DACL = 4

Dim obj as IADs
Dim sd as IADsSecurityDescriptor
Dim oOptions as IADsObjectOptions

' Bind to the object.
Set obj = GetObject("LDAP://.....")

' Get the IADsSecurityDescriptor.
Set sd = obj.Get("ntSecurityDescriptor")

' Modify the DACL as required.

' Get the IADsObjectOptions for the object - not the IADsSecurityDescriptor.
Set oOptions = obj

' Set options so that only the DACL will be updated.
oOptions.SetOption ADS_OPTION_SECURITY_MASK, ADS_INFO_DACL

' Update the security descriptor.
obj.Put "ntSecurityDescriptor", sd
obj.SetInfo
```


The following code example shows how to display data from a security descriptor.


```vb
' Get the security descriptor.
Dim x As IADs
Dim sd As IADsSecurityDescriptor

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set sd = Nothing

```


The following code example shows how to  display data from a security descriptor of a directory object.


```cpp
HRESULT DisplaySD(IADs *pObj)
{
    IADsSecurityDescriptor *pSD = NULL;
    BSTR bstr = NULL;
    long lVal = 0;    
    HRESULT hr = S_OK;
    VARIANT var;
    
    VariantInit(&var);

    if(pObj==NULL)
    {
        return E_FAIL;
    }
    
    hr = pObj->Get(CComBSTR("ntSecurityDescriptor"), &var);
    if(FAILED(hr)){goto Cleanup;}
    
    
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
    if(FAILED(hr)){goto Cleanup;}
    
   hr = pSD->get_Control(&lVal);
   printf("SD Control = %d\n",lVal);

   hr = pSD->get_Owner(&bstr);
   printf("SD Owner   = %S\n",bstr);
   SysFreeString(bstr);

   hr = pSD->get_Group(&bstr);
   printf("SD Group   = %S\n",bstr);
   SysFreeString(bstr);

   hr = pSD->get_Revision(&lVal);
   printf("SD Revision= %d\n",lVal);
        
Cleanup:
    VariantClear(&var);
    if(pSD) pSD->Release();
    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb">Creating a Security Descriptor for a New Directory
    Object</a>



<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/32b786d2-e676-4402-ad22-550de9289494">Null DACLs and Empty DACLs</a>
 

 

