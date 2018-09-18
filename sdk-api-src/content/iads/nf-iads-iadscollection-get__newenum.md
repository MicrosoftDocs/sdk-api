---
UID: NF:iads.IADsCollection.get__NewEnum
title: IADsCollection::get__NewEnum
author: windows-sdk-content
description: The IADsCollection::get__NewEnum method gets a dependent enumerator object that implements IEnumVARIANT for this ADSI collection object. Be aware that there are two underscore characters in the function name (get__NewEnum).
old-location: adsi\iadscollection_get__newenum.htm
tech.root: ADSI
ms.assetid: db2630d0-26be-4cf1-811e-fc1d2007dda5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsCollection interface [ADSI],get__NewEnum method, IADsCollection.get__NewEnum, IADsCollection::get__NewEnum, _ds_iadscollection_get__newenum, adsi.iadscollection__get____newenum, adsi.iadscollection_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsCollection interface, iads/IADsCollection::get__NewEnum
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
 - IADsCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsCollection::get__NewEnum


## -description


The <b>IADsCollection::get__NewEnum</b> method gets a dependent enumerator object that implements  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> for this ADSI collection object. Be aware that there are two underscore characters in the function name (<b>get__NewEnum</b>).


## -parameters




### -param ppEnumerator [out]

Pointer to a pointer to the  <a href="_com_iunknown">IUnknown</a> interface on the enumerator object for this collection.


## -returns



This method supports the standard return values including <b>S_OK</b>, <b>E_FAIL</b>, or <b>E_NOTIMPL</b>. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



When a server supports paged search and the client has specified the page limit greater than the maximum search results allowed on the server, the <b>IADsCollection::get__NewEnum</b> method returns errors in the following ways:

<ul>
<li>If the server returns an error with no results, the function returns the error only.</li>
<li>If the server returns partial results with or without an error, for example, the maximum search results allowed on the server, the function returns the partial results from the server to the user.</li>
<li>If the server returns all results with or without an error, for example, maximum search results on each page and all results through multiple pages, the function returns all the results from the server to the user.</li>
</ul>

#### Examples

The <b>For Each</b>…<b>In</b>…<b>Next</b> statement in the following Visual Basic code example invokes <b>get__NewEnum</b> method implicitly.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim fso As IADsFileServiceOperations 
On Error GoTo Cleanup

Set fso = GetObject("WinNT://myComputer/Fabrikam01") 
 
Dim coll As IADsCollection
Set coll = fso.Sessions
 
' The following statement invokes IADsCollection::get__NewEnum.
For Each session In coll 
   MsgBox "Session name: " &amp; session.Name
Next session

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred... " &amp; Err.Number)
    End If
    Set fso = Nothing</pre>
</td>
</tr>
</table></span></div>
The following C++ code example shows how <b>IADsCollection::get__NewEnum</b> is used to enumerate active file service sessions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumCollection(IADsCollection *);

HRESULT GetACollectionOfSessions()
{
    LPWSTR adspath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;

    // Bind to file service operations.
    IADsFileServiceOperations *pFso = NULL;
    hr = ADsGetObject(adspath,
                      IID_IADsFileServiceOperations,
                      (void**)&amp;pFso);
    if(FAILED(hr)) {goto Cleanup;}

    // Get the pointer to the collection.
    hr = pFso-&gt;Sessions(&amp;pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = EnumCollection(pColl);

Cleanup:
    if(pColl) pColl-&gt;Release();
    if(pFso) pFso-&gt;Release();

    return hr;
}

HRESULT EnumCollection(IADsCollection *pColl)
{
    IUnknown *pUnk=NULL;
    HRESULT hr = S_OK;
    // Get the Enumerator object on the collection object.
    hr = pColl-&gt;get__NewEnum(&amp;pUnk);
    if(FAILED(hr)) {goto Cleanup;}

    IEnumVARIANT *pEnum;
    hr = pUnk-&gt;QueryInterface(IID_IEnumVARIANT,(void**)&amp;pEnum);
    if(FAILED(hr)) {goto Cleanup;}

    // Enumerate the collection.
    BSTR bstr = NULL;
    VARIANT var;
    IADs *pADs = NULL;
    ULONG lFetch;
    IDispatch *pDisp = NULL;

    VariantInit(&amp;var);
    hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
    while(hr == S_OK)
    {
        if (lFetch == 1)    
        {
             pDisp = V_DISPATCH(&amp;var);
             pDisp-&gt;QueryInterface(IID_IADs, (void**)&amp;pADs);
             pADs-&gt;get_Name(&amp;bstr);
             printf("Session name: %S\n",bstr);
             SysFreeString(bstr);
             pADs-&gt;Release();
        }
        VariantClear(&amp;var);
        pDisp-&gt;Release();
        pDisp = NULL;
        hr = pEnum-&gt;Next(1, &amp;var, &amp;lFetch);
    };
    

Cleanup:
    if(pDisp) pDisp-&gt;Release();
    if(pUnk) pUnk-&gt;Release();
    if(pColl) pColl-&gt;Release();
    if(pEnum) pEnum-&gt;Release();
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="_com_iunknown">IUnknown</a>
 

 

