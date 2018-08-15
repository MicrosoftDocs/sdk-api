---
UID: NF:iads.IADsContainer.Delete
title: IADsContainer::Delete
author: windows-sdk-content
description: Deletes a specified directory object from this container.
old-location: adsi\iadscontainer_delete.htm
old-project: ADSI
ms.assetid: 2f3873e0-376e-4212-a28d-bd9bc112f6cf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Delete, Delete method [ADSI], Delete method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],Delete method, IADsContainer.Delete, IADsContainer::Delete, _ds_iadscontainer_delete, adsi.iadscontainer__delete, adsi.iadscontainer_delete, iads/IADsContainer::Delete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsContainer.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsContainer::Delete


## -description


The <b>IADsContainer::Delete</b> method deletes a specified directory object from this container.


## -parameters




### -param bstrClassName




### -param bstrRelativeName [in]

Name of the object as it is known in the underlying directory and identical to the name retrieved with the  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs::get_Name</a> method.


#### - bstrClass [in]

The schema class object to delete. The name is that returned from the  <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs::get_Class</a> method. Also, <b>NULL</b> is a valid option for this parameter.   Providing <b>NULL</b> for this parameter is the only way to deal with defunct schema classes. If an instance was created before the class became defunct, the only way to  delete the instance of the defunct class is to call <b>IADsContainer::Delete</b> and provide <b>NULL</b> for this parameter.


## -returns



This method supports the standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The object to be deleted must be a leaf object or a childless subcontainer. To delete a container and its children, that is, a subtree, use  <a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a>.

The specified object is immediately removed after calling  <b>IADsContainer::Delete</b> and calling  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> on the container object is unnecessary.

When using the  <b>IADsContainer::Delete</b> method to delete an object in C/C++ applications, release the interface pointers to that object as well. This is because the method removes the object from the underlying directory immediately, but leave intact any interface pointers held, in memory, by the application, for the deleted object. If not released, confusion can occur in that you may call  <a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a> and  <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> on the deleted object without error, but will receive an error when you call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> or  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> on the deleted object.


#### Examples

The following code example deletes a user object from the container in Active Directory.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim cont as IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
cont.Delete "user", "CN=JeffSmith"

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set cont = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example deletes a user object from the container under WinNT provider.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim cont as IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("WinNT://Fabrikam")
cont.Delete "user", "jeffsmith"

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set cont = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example deletes a user using  <b>IADsContainer::Delete</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = S_OK;
IADsContainer *pCont=NULL;
 
CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine", 
                  IID_IADsContainer, 
                  (void**) &amp;pCont);
if ( !SUCCEEDED(hr) )
{
     return hr;
}
 
hr = pCont-&gt;Delete(CComBSTR("user"), CComBSTR("JeffSmith"));
pCont-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error
  Codes</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs::get_Class</a>



<b>IADs::get_Name</b>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/9498ef4d-7a03-487f-91a7-189f17a38a24">IADsContainer::Create</a>



<a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a>
 

 

