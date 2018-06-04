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

# IADsCollection::GetObject


## -description


The <b>IADsCollection::GetObject</b> method retrieves an item of the collection.


## -parameters




### -param bstrName [in]

The null-terminated Unicode string that specifies the name of the item. This is the same name passed to  <a href="https://msdn.microsoft.com/c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d">IADsCollection::Add</a> when the item is added to the collection.


### -param pvItem






#### - pvarItem [in]

Current value of the item. For an object, this corresponds to the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer on the object.


## -returns



This method supports the standard return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



If you know the name of a session in the <b>Sessions</b> collection, call the <b>IADsCollection::GetObject</b> method explicitly to retrieve the session object.


#### Examples

The following Visual Basic code example shows how to retrieve a named session object from a collection of active file service sessions.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim fso As IADsFileServiceOperations 
Dim ses As IADsSession
Dim coll As IADsCollection
Dim mySessionName As String

Set fso = GetObject("WinNT://myComputer/FabrikamServer") 
Set coll = fso.Sessions

' Insert code to set mySessionName to the name of mySession.
 
' The following statement invokes IADsCollection::GetObject.
Set ses = coll.GetObject(mySessionName)</pre>
</td>
</tr>
</table></span></div>
The following C++ code example shows how to retrieve a named session object from a collection of active file service sessions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT GetASessionObjectFromCollection(BSTR mySession)
{
    LPWSTR adspath = L"WinNT://myComputer/FabrikamServer";
    IUnknown *pUnk=NULL;
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;
    IADsFileServiceOperations *pFso = NULL;
    IADs *pADsObj = NULL;
    VARIANT varObj;
    BSTR bstrObj = NULL;

    VariantInit(&amp;varObj);
    hr = ADsGetObject(adspath, 
                      IID_IADsFileServiceOperations,
                      (void**)&amp;pFso);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFso-&gt;Sessions(&amp;pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pColl-&gt;GetObject(mySession, &amp;varObj);
    V_DISPATCH(&amp;varObj)-&gt;QueryInterface(IID_IADs,(void**)&amp;pADsObj);
    hr = pADsObj-&gt;get_Class(&amp;bstrObj);
    printf("Class of the object obtained from GetObject: %S\n",
             bstrObj);

Cleanup:
    if(bstrObj) SysFreeString(bstrObj);
    if(pFso) pFso-&gt;Release();
    VariantClear(&amp;varObj);
    if(pADsObj) pADsObj-&gt;Release();
    if(pColl) pColl-&gt;Release();

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error
  Codes</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d">IADsCollection::Add</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

