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

# ITuningSpaceContainer::get_Item


## -description



The <b>get_Item</b> method retrieves a tuning space with the specified ID.




## -parameters




### -param varIndex [in]

<b>VARIANT</b> that specifies the ID of the tuning space.


### -param TuningSpace






#### - ppTuningSpace [out]

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
 

 

