---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IADsContainer::get__NewEnum


## -description


The <b>IADsContainer::get__NewEnum</b> method Retrieves an enumerator object for the container. The 
  enumerator object implements the  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface to enumerate the children of the container object.


## -parameters




### -param retval






#### - ppEnumerator [out]

Pointer to an <a href="_com_iunknown">IUnknown</a> pointer that receives the enumerator object. The caller must release this interface when it is no longer required.


## -returns



This method supports the standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



There are two underscore characters ("__") in the function name between "get" and "NewEnum".

In Visual Basic, use the <b>For</b><b>Each</b>… statement to invoke the <b>IADsContainer::get__NewEnum</b> method implicitly.

In C/C++, use the  <a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a>,  <a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>, and <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">AdsFreeEnumerator</a> helper functions.


#### Examples

The following code example shows how to enumerate child objects in a container.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim cont As IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
For Each obj In cont
  Debug.Print obj.Name
Next

Cleanup:
    If(Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set cont = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to enumerate the object contained in a container.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
LPUNKNOWN pUnk = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ulong lFetch;
IADs *pADs = NULL;
 
// In this sample, skip error checking.
ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM", 
                        IID_IADsContainer, (void**) &amp;pCont);
pCont-&gt;get__NewEnum(&amp;pUnk);
pCont-&gt;Release();
 
pUnk-&gt;QueryInterface(IID_IEnumVARIANT, (void**) &amp;pEnum);
pUnk-&gt;Release();
 
// Enumerate. 
HRESULT hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
while(SUCCEEDED(hr) &amp;&amp; lFetch &gt; 0)
{
    if (lFetch == 1)
    {
        BSTR bstr;

        pDisp = V_DISPATCH(&amp;var);
        pDisp-&gt;QueryInterface(IID_IADs, (void**)&amp;pADs); 
        pDisp-&gt;Release();
        hr = pADs-&gt;get_Name(&amp;bstr);
        if(SUCCEEDED(hr))
        {
            SysFreeString(bstr);
        }

        pADs-&gt;Release();
    }

    VariantClear(&amp;var);
    hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
};

 
pEnum-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e4fdec19-bccf-49ec-8a95-29e096c4c9c1">ADsBuildEnumerator</a>



<a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>



<a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">AdsFreeEnumerator</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="_com_iunknown">IUnknown</a>
 

 

