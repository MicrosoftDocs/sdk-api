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

# IADsPropertyList::PurgePropertyList


## -description


The <b>IADsPropertyList::PurgePropertyList</b> method deletes all items from the property list.


## -parameters






## -returns



This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



When the <b>PurgePropertyList</b> method is called, all the items are removed from the cache. Thus, calling  <a href="https://msdn.microsoft.com/1de86caa-c14c-4dc0-bf56-5fa33279e30a">GetPropertyItem</a> after that will generate an error. Be aware that <b>PurgePropertyList</b> only affects the contents of the cache and does not affect the properties on the actual object in the directory; that is, calling  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a> after calling <b>PurgePropertyList</b> does not delete the properties on the directory object.


#### Examples

The following code example shows how to implement <b>IADsPropertyList::PurgePropertyList</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim propList As IADsPropertyList
 
On Error GoTo Cleanup

Set propList = GetObject("LDAP://dc03/DC=Fabrikam,DC=com")
propList.GetInfo
 
propList.PurgePropertyList
 
'- None of GetPropertyItem should work, because the list is purged.
'- The following line should generate error.
Set propEntry = propList.GetPropertyItem("adminDescription", ADSTYPE_CASE_IGNORE_STRING)

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If

    Set propList = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows the effect produced by a call to <b>IADsPropertyList::PurgePropertyList</b>.  For more information about the <b>GetPropertyCache</b>  function and a code example, see <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPropertyList *GetPropertyCache(LPWSTR);
 
void TestPurgePropertyList()
{
    IADsPropertyList *pList;
    pList=GetPropertyCache(L"WinNT://myComputer,computer");
 
    long count;

    if(pList)
    {
        pList-&gt;get_PropertyCount(&amp;count);
        printf("Number of properties before purging: %d\n",count);
 
        count = -1;
        pList-&gt;PurgePropertyList();
        pList-&gt;get_PropertyCount(&amp;count);
        printf("Number of properties after purging: %d\n",count);
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="https://msdn.microsoft.com/1de86caa-c14c-4dc0-bf56-5fa33279e30a">IADsPropertyList::GetPropertyItem</a>
 

 

