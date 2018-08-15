---
UID: NF:iads.IADsCollection.Remove
title: IADsCollection::Remove
author: windows-sdk-content
description: The IADsCollection::Remove method removes the named item from this ADSI collection object.
old-location: adsi\iadscollection_remove.htm
old-project: ADSI
ms.assetid: 21ce80fe-542b-4350-b66c-fa26f62ca611
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsCollection interface [ADSI],Remove method, IADsCollection.Remove, IADsCollection::Remove, Remove, Remove method [ADSI], Remove method [ADSI],IADsCollection interface, _ds_iadscollection_remove, adsi.iadscollection__remove, adsi.iadscollection_remove, iads/IADsCollection::Remove
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
 - IADsCollection.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsCollection::Remove


## -description


The <b>IADsCollection::Remove</b> method removes the named item from this ADSI collection object.


## -parameters




### -param bstrItemToBeRemoved [in]

The null-terminated Unicode string that specifies the name of the item as it was specified by  <a href="https://msdn.microsoft.com/c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d">IADsCollection::Add</a>.


## -returns



This method supports the standard return values, including <b>S_OK</b>. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Collections for a directory service can also consist of a set of immutable objects.

Collections that do not support direct removal of items are required to return <b>E_NOTIMPL</b>.


#### Examples

The following Visual Basic code example shows how to remove a named session object from a collection of active file service sessions.

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

On Error GoTo Cleanup

Set fso = GetObject("WinNT://myComputer/FabrikamServer") 
Set coll = fso.Sessions

' Insert code to set mySessionName to the name of the mySession 
' session object.
 
' The following statement invokes IADsCollection::Remove.
coll.Remove mySessionName

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set fso = Nothing
    Set ses = Nothing
    Set coll = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following C++ code example shows how to remove a named session object from a collection of active file service sessions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT RemoveASessionObjectFromCollection()
{
    LPWSTR adspath = L"WinNT://myComputer/FabrikamServer";
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;
    IADsFileServiceOperations *pFso = NULL;

    hr = ADsGetObject(adspath,IID_IADsFileServiceOperations,(void**)&amp;pFso);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFso-&gt;Sessions(&amp;pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pColl-&gt;Remove(CComBSTR("MySession"));

Cleanup
    if(pFso) pFso-&gt;Release();
    if(pColl) pColl-&gt;Release();

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4552552b-c008-439a-95bf-eaf9ffd28b5f">IADsCollection</a>



<a href="https://msdn.microsoft.com/c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d">IADsCollection::Add</a>
 

 

