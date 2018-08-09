---
UID: NF:iads.IADsCollection.GetObject
title: IADsCollection::GetObject
author: windows-sdk-content
description: Retrieves an item of the collection.
old-location: adsi\iadscollection_getobject.htm
old-project: ADSI
ms.assetid: 04b33451-505e-43de-8db4-3e37f9909ea6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetObject, GetObject method [ADSI], GetObject method [ADSI],IADsCollection interface, IADsCollection interface [ADSI],GetObject method, IADsCollection.GetObject, IADsCollection::GetObject, _ds_iadscollection_getobject, adsi.iadscollection__getobject, adsi.iadscollection_getobject, iads/IADsCollection::GetObject
ms.prod: windows
ms.technology: windows-sdk
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
 - IADsCollection.GetObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

