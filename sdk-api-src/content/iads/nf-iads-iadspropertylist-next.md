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

# IADsPropertyList::Next


## -description


The <b>IADsPropertyList::Next</b> method gets the next item in the property list. The returned item is a Property Entry object.


## -parameters




### -param pVariant [out]

Address of a caller-allocated variable that contains the value of the next item in the property list. The return value of <b>VT_DISPATCH</b> refers to an  <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to an object implementing the  <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> interface.


## -returns



This method supports the standard <b>HRESULT</b> values, including <b>S_OK</b> if the item is obtained. When the last item in the list is returned, the return value that is returned will differ depending on which provider is used. The following codes are used to indicate that the last item in the list was obtained:

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



You must clear <i>pVariant</i> using <b>VariantClear</b> when the value returned by the <b>Next</b> method is no longer required.


#### Examples

The following code example shows how to walk through a property list using the <b>Next</b> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim propList As IADsPropertyList
Dim v as Variant
Dim propVal As IADsPropertyValue
 
On Error Resume Next
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
Set v = propList.Next()
While (Not (IsNull(v)) And Err.Number = 0)
    Set propEnty = v
    Debug.Print v.Name
    Debug.Print v.AdsType
    
    Set v = propList.Next    
Wend</pre>
</td>
</tr>
</table></span></div>
The following C++ code example shows how to work the <b>IADsPropertyList::Next</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>////////////////////////////////////
// Function used to retrieve an entry using the 
// IADsPropertyList::Next method.
 
//     name: GetNextEntry
//    input: IADsPropertyList*
//   return: IADsPropertyEntry
//     uses: IADsPropertyList::Next
/////////////////////////////////////////////////////////
IADsPropertyEntry* GetNextEntry(IADsPropertyList* pList)
{
    VARIANT var;
    VariantInit(&amp;var);
    IADsPropertyEntry *pEntry;

    if(!pList)
    {
        _tprintf("An error has occurred.");
        return NULL;
    }
 
    HRESULT hr = pList-&gt;Next(&amp;var);
    hr = V_DISPATCH(&amp;var)-&gt;QueryInterface(IID_IADsPropertyEntry,
                                         (void**)&amp;pEntry);
    VariantClear(&amp;var);
    return pEntry;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

