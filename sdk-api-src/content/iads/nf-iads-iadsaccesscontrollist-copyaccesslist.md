---
UID: NF:iads.IADsAccessControlList.CopyAccessList
title: IADsAccessControlList::CopyAccessList
author: windows-sdk-content
description: The IADsAccessControlList::CopyAccessList method copies every access control entry (ACE) in the access-control list (ACL) to the caller's process space.
old-location: adsi\iadsaccesscontrollist_copyaccesslist.htm
tech.root: ADSI
ms.assetid: 3f4c89ec-1144-4886-981a-75353d2dfe8b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CopyAccessList, CopyAccessList method [ADSI], CopyAccessList method [ADSI],IADsAccessControlList interface, IADsAccessControlList interface [ADSI],CopyAccessList method, IADsAccessControlList.CopyAccessList, IADsAccessControlList::CopyAccessList, _ds_iadsaccesscontrollist_copyaccesslist, adsi.iadsaccesscontrollist__copyaccesslist, adsi.iadsaccesscontrollist_copyaccesslist, iads/IADsAccessControlList::CopyAccessList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IADsAccessControlList.CopyAccessList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsAccessControlList::CopyAccessList


## -description


The <b>IADsAccessControlList::CopyAccessList</b> method copies every access control entry (ACE) in the access-control list (ACL) to the caller's process space.


## -parameters




### -param ppAccessControlList [out]

Address of an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to an ACL as the copy of the original access list. If this parameter is <b>NULL</b> on return, no copies of the ACL could be made.


## -returns



This method returns the standard return values.

For more information about  other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The caller must call <b>Release</b> on the copy of ACEs through their <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointers.


#### Examples

The following code example shows how to copy an ACL from one ADSI object to another.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList
Dim CopyDacl As IADsAccessControlList
 
' Get the ACL from one object.
Set x = GetObject("LDAP://OU=Sales, DC=activeD,DC=mydomain,DC=fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Set CopyDacl = Dacl.CopyAccessList()
 
' Copy the ACL to another object in the Directory.
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
sd.DiscretionaryAcl = CopyDacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set x = Nothing
    Set sd = Nothing
    Set Dacl = Nothing
    Set CopyDacl = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example copies the ACL from the source object to the target object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CopyACL(IADs *pSource, IADs *pTarget)
{
    IADsSecurityDescriptor *pSourceSD = NULL;
    IADsSecurityDescriptor *pTargetSD = NULL;    
    IDispatch *pDisp = NULL;
    
    HRESULT hr = S_OK;
    VARIANT varSource, varTarget;
    
    VariantInit(&amp;varSource);
    VariantInit(&amp;varTarget);

    if((pSource==NULL) || (pTarget==NULL))
    {
        return E_FAIL;
    }
    
    hr = pSource-&gt;Get(CComBSTR("ntSecurityDescriptor"), &amp;varSource);
    if(FAILED(hr))
    {
        goto Cleanup;
    }
    
    hr = pTarget-&gt;Get(CComBSTR("ntSecurityDescriptor"), &amp;varTarget);
    if(FAILED(hr))
    {
        goto Cleanup;
    }
    
    hr = V_DISPATCH(&amp;varSource)-&gt;QueryInterface(IID_IADsSecurityDescriptor,
                    (void**)&amp;pSourceSD);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    

    hr = V_DISPATCH(&amp;varTarget)-&gt;QueryInterface(IID_IADsSecurityDescriptor,
                    (void**)&amp;pTargetSD);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    
    
    hr = pSourceSD-&gt;get_DiscretionaryAcl(&amp;pDisp);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    

    hr = pTargetSD-&gt;put_DiscretionaryAcl(pDisp);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    
    
    hr = pTarget-&gt;SetInfo();
        
Cleanup:
    VariantClear(&amp;varSource);
    VariantClear(&amp;varTarget);
    if(pSourceSD) 
    {
        pSourceSD-&gt;Release();
    }
    if(pTargetSD) 
    {
        pTargetSD-&gt;Release();
    }
    if(pDisp) 
    {
        pDisp-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>
 

 

