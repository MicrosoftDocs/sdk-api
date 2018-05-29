---
UID: NN:iads.IADsAccessControlList
title: IADsAccessControlList
author: windows-sdk-content
description: The IADsAccessControlList interface is a dual interface that manages individual access-control entries (ACEs).
old-location: adsi\iadsaccesscontrollist.htm
old-project: ADSI
ms.assetid: de92d9cc-bc9d-4dc5-aa79-01f4d3050c35
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: AccessControlList, IADsAccessControlList, IADsAccessControlList interface [ADSI], IADsAccessControlList interface [ADSI],described, _ds_iadsaccesscontrollist, adsi.iadsaccesscontrollist, iads/IADsAccessControlList
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsAccessControlList
-	AccessControlList
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsAccessControlList interface


## -description


The <b>IADsAccessControlList</b> interface is a dual interface that manages individual access-control entries (ACEs).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsAccessControlList</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsAccessControlList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsAccessControlList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/663be55a-29d6-4a8a-adf2-024762413fc3">AddAce</a>
</td>
<td align="left" width="63%">
Adds an entry to the ACL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f4c89ec-1144-4886-981a-75353d2dfe8b">CopyAccessList</a>
</td>
<td align="left" width="63%">
Copies the ACL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/569f3bfa-3933-43b3-9d16-c3d4382cfa9f">get__NewEnum</a>
</td>
<td align="left" width="63%">
Gets a pointer to the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29c1ffcc-5a66-4ee3-889a-747953c604a4">RemoveAce</a>
</td>
<td align="left" width="63%">
Removes an entry from the ACL.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsAccessControlList</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cb68bb61-4216-4f69-bea1-ab7f98937a27">AceCount</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets number of ACEs in the ACL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cb68bb61-4216-4f69-bea1-ab7f98937a27">AclRevision</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the ACL revision number.

</td>
</tr>
</table> 


## -remarks



An access-control list (ACL) is a collection of ACEs that can provide more specific access control to the same ADSI object for different clients. In general, different providers implement different access controls and therefore the behavior of the object is specific to the provider.  For more information, see  the provider documentation. For more information about Microsoft providers, see  <a href="https://msdn.microsoft.com/419d7953-a879-4d6c-be74-173d76c3f932">ADSI System Providers</a>. Currently, only the LDAP provider supports access controls.

Before you can work with an object ACE, first obtain the ACL to which they belong. ACLs are managed by security descriptors and can be of either discretionary ACL and system ACL. For more information, see 
  <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>.

Using the properties and methods of the <b>IADsAccessControlList</b> interface, you can retrieve and enumerate ACEs, add new entries to the list, or remove existing entries.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To manage access controls over an ADSI</b>

<ol>
<li>First, retrieve the security descriptor of the object that implements the  <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface.</li>
<li>Second, retrieve the ACL from the security descriptor.</li>
<li>Third, work with the ACE, or ACEs, of the object in the ACL.</li>
</ol>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To make any new or modified ACEs persistent</b>

<ol>
<li>First, add the ACE to the ACL.</li>
<li>Second, assign the ACL to the security descriptor.</li>
<li>Third, commit the security descriptor to the directory store.</li>
</ol>
For more information about DACLs, see <a href="https://msdn.microsoft.com/32b786d2-e676-4402-ad22-550de9289494">Null DACLs and Empty DACLs</a>.


#### Examples

The following code example shows  how to work with access control entries of a discretionary ACL.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim X As IADs
Dim Namespace As IADsOpenDSObject
Dim SecurityDescriptor As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup
 
Set Namespace = GetObject("LDAP://")
Set X= Namespace.OpenDSObject("LDAP://DC=Fabrikam,DC=Com, vbNullString, vbNullString,  ADS_SECURE_AUTHENTICATION)
 
Set SecurityDescriptor = X.Get("ntSecurityDescriptor")
Debug.Print SecurityDescriptor.Owner
Debug.Print SecurityDescriptor.Group
 
Set Dacl = SecurityDescriptor.DiscretionaryAcl
Debug.Print Dacl.AceCount
 
For Each Obj In Dacl
   Debug.Print Obj.Trustee
   Debug.Print Obj.AccessMask
   Debug.Print Obj.AceFlags
   Debug.Print Obj.AceType
Next

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set X = Nothing
    Set Namespace = Nothing
    Set SecurityDescriptor = Nothing
    Set Dacl = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example enumerates ACEs from a DACL.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&amp;var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&amp;pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs-&gt;Get(CComBSTR("ntSecurityDescriptor"), &amp;var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&amp;var);

hr = pDisp-&gt;QueryInterface(IID_IADsSecurityDescriptor,(void**)&amp;pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp-&gt;Release();


pSD-&gt;get_DiscretionaryAcl(&amp;pDisp);

hr = pDisp-&gt;QueryInterface(IID_IADsAccessControlList,(void**)&amp;pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&amp;var);

Cleanup:
    if(pADs) pADs-&gt;Release();
    if(pDisp) pDisp-&gt;Release();
    if(pSD) pSD-&gt;Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&amp;var);
    
    hr = pSD-&gt;get_DiscretionaryAcl(&amp;pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp-&gt;QueryInterface(IID_IADsAccessControlList,(void**)&amp;pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL-&gt;get__NewEnum(&amp;pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk-&gt;QueryInterface(IID_IEnumVARIANT,(void**)&amp;pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum-&gt;Next(1,&amp;var,&amp;nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&amp;var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&amp;var);
            hr = pDisp-&gt;QueryInterface(IID_IADsAccessControlEntry,(void**)&amp;pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE-&gt;get_Trustee(&amp;bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE-&gt;Release();
                pACE = NULL;
                pDisp-&gt;Release();
                pDisp = NULL;
            }       
            
            VariantClear(&amp;var);
        }       
        hr = pEnum-&gt;Next(1,&amp;var,&amp;nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp-&gt;Release();
    if(pACL) pACL-&gt;Release();
    if(pACE) pACE-&gt;Release();
    if(pEnum) pEnum-&gt;Release();
    if(pUnk) pUnk-&gt;Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/32b786d2-e676-4402-ad22-550de9289494">Null DACLs and Empty DACLs</a>
 

 

