---
UID: NN:iads.IADsContainer
title: IADsContainer
author: windows-sdk-content
description: The IADsContainer interface enables an ADSI container object to create, delete, and manage contained ADSI objects. Container objects represent hierarchical directory trees, such as in a file system, and to organize the directory hierarchy.
old-location: adsi\iadscontainer.htm
tech.root: ADSI
ms.assetid: 6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsContainer, IADsContainer interface [ADSI], IADsContainer interface [ADSI],described, _ds_iadscontainer, adsi.iadscontainer, iads/IADsContainer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IADsContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IADsContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a006253-ccb4-4f13-93b5-297db17f7c2e">CopyHere</a>
</td>
<td align="left" width="63%">
Copies an object to the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9498ef4d-7a03-487f-91a7-189f17a38a24">Create</a>
</td>
<td align="left" width="63%">
Creates an object in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3873e0-376e-4212-a28d-bd9bc112f6cf">Delete</a>
</td>
<td align="left" width="63%">
Deletes an object in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b268efb8-59cd-41ef-b96c-583ae476432e">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator object for the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df8b1eae-1138-4e55-af6e-17c6105ca9c1">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an interface for a directory object in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/132b1cdc-6fb5-43b1-a5de-3b25c361e8e1">MoveHere</a>
</td>
<td align="left" width="63%">
Moves an object to the container.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsContainer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/74d348bf-7b7f-4971-ba03-f77940600674">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the number of directory objects in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/74d348bf-7b7f-4971-ba03-f77940600674">Filter</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the filter on the schema classes to use for an enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/74d348bf-7b7f-4971-ba03-f77940600674">Hints</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the properties to retrieve for each object that is enumerated by the container.

</td>
</tr>
</table> 


## -remarks



To determine if an object is a container, use the <a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">IADsClass.Container</a> property of the object.

When you bind to a container object using its GUID (or SID), you can only perform specific operations on the container object. These operations include examination of the object attributes and enumeration of the object's immediate children. These operations are shown in the following code example.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim con As IADsContainer
Dim obj As IADs
Set con = GetObject("LDAP://svr01/&lt;GUID=xxxx&gt;")
con.Filter = Array("user")
For Each item In con
    debug.print item.Name " &amp;  " of " &amp; item.Class
Next</pre>
</td>
</tr>
</table></span></div>
All other operations, that is, <b>GetObject</b>, <b>Create</b>, <b>Delete</b>, <b>CopyHere</b>, and <b>MoveHere</b> are not supported in the container's GUID representation. For example, the last line of the following code example will result in an error.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim con As IADsContainer
Dim obj As IADs
Set con = GetObject("LDAP://svr01/&lt;GUID=xxxx&gt;")
Set obj = con.GetObject("user", "CN=Jeff Smith")</pre>
</td>
</tr>
</table></span></div>
Binding, using GUID (or SID), is intended for low overhead and, thus, fast binds, which are often used for object introspection.

To call these methods of the container bound with its GUID (or SID), rebind to the object using its distinguished name.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim conGUID, conDN As IADsContainer
Dim obj As IADs
Set conGUID = GetObject("LDAP://svr/&lt;GUID=xxxx&gt;")
Set conDN=GetObject("LDAP://svr/" &amp; conGUID.Get("distinguishedName"))
Set obj = conDN.GetObject("user", "CN=Jeff Smith")</pre>
</td>
</tr>
</table></span></div>
For more information about object GUID representation, see <a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">IADs.GUID</a>.


#### Examples

The following code example determines if an ADSI object is a container.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim obj As IADs
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
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set obj = Nothing
    Set cls = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example determines if an ADSI object is a container.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pADs = NULL;
IADsClass *pCls = NULL;
HRESULT hr = S_OK;
BSTR bstr;

hr = ADsGetObject(L"WinNT://myComputer,computer", IID_IADs, (void**)&amp;pADs);
if(FAILED(hr)){return;}

pADs-&gt;get_Schema(&amp;bstr);
hr = ADsGetObject(bstr, IID_IADsClass, (void**)&amp;pCls);
pADs-&gt;Release();
SysFreeString(bstr);

if(FAILED(hr)){return;}

VARIANT_BOOL isContainer;
pCls-&gt;get_Container(&amp;isContainer);

if(isContainer) 
    printf("Object is a container.\n");
else
    printf("Object is not a container.\n");

pCls-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8">Creating and Deleting Objects</a>



<a href="https://msdn.microsoft.com/d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12">IADs::get_GUID</a>



<a href="https://msdn.microsoft.com/191f6873-c4bd-4e71-9d23-478454b7cec2">IADsClass::get_Container</a>



<a href="https://msdn.microsoft.com/edac671e-9ab1-4211-9fd7-1a0b965196b4">IADsNamespaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

