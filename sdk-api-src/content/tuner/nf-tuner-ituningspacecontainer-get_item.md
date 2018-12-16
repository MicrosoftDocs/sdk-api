---
UID: NF:tuner.ITuningSpaceContainer.get_Item
title: ITuningSpaceContainer::get_Item
author: windows-sdk-content
description: The get_Item method retrieves a tuning space with the specified ID.
old-location: mstv\ituningspacecontainer_get_item.htm
tech.root: mstv
ms.assetid: 02e17867-dc72-481a-8693-68e9b0288bba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],get_Item method, ITuningSpaceContainer.get_Item, ITuningSpaceContainer::get_Item, ITuningSpaceContainerget_Item, get_Item, get_Item method [Microsoft TV Technologies], get_Item method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_get_item, tuner/ITuningSpaceContainer::get_Item
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaceContainer.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpaceContainer::get_Item


## -description



The <b>get_Item</b> method retrieves a tuning space with the specified ID.




## -parameters




### -param varIndex [in]

<b>VARIANT</b> that specifies the ID of the tuning space.


### -param TuningSpace [out]

Address of an <a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace</a> interface pointer that will be set to the returned interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



Tuning spaces are identified by ID number. The ID number is unique within the collection. The range of valid IDs is not guaranteed to be contiguous; there may be holes if tuning spaces are added and then removed.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr &lt;ITuningSpaceContainer&gt;  pTuningSpaceContainer;
// Create the SystemTuningSpaces object (not shown).

long cCount = 0;
long ID = 1; // zero is not a valid ID.
hr = pTuningSpaceContainer-&gt;get_Count(&amp;cCount);
if (SUCCEEDED(hr))
{
    while (cCount)
    {
        CComPtr&lt;ITuningSpace&gt; pTuningSpace;
        CComVariant varIndex(ID);
        hr = pITuningSpaceContainer-&gt;get_Item(varIndex, &amp;pTuningSpace);
        if (SUCCEEDED(hr))
        {
             // pTuningSpace now points to the tuning space with this ID.
             --cCount;
        }
        ID++; // incremement for the next ID.
    }
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

