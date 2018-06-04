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

# ITuningSpaceContainer::TuningSpacesForName


## -description



The <b>TuningSpacesForName</b> method retrieves a collection of tuning spaces that match the specified name.




## -parameters




### -param Name [in]

String that contains a regular expression to match against either the friendly name or the unique name of the tuning space.


### -param NewColl






#### - ppTuningSpaces [out]

Address of variable that receives an <a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces</a> interface pointer. Use this interface to enumerate the collection. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The returned collection might be empty, if no tuning spaces match the name.


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

// Try to match any tuning spaces named "Local (something) Cable".
CComPtr&lt;ITuningSpaces&gt; pTunes;
CComBSTR bstrName("Local.*Cable");
hr = pITuningSpaceContainer-&gt;TuningSpacesForName(bstrName, &amp;pTunes);
if (SUCCEEDED(hr))
{
    // Find the size of the returned collection.
    long cCount = 0;
    hr = pTunes-&gt;get_Count(&amp;cCount);
    if (SUCCEEDED(hr) &amp;&amp; (cCount &gt; 0))
    {
        // Enumerate the collection.
        CComPtr&lt;IEnumTuningSpaces&gt; pTuneEnum;
        hr = pTunes-&gt;get_EnumTuningSpaces(&amp;pTuneEnum);
        if (SUCCEEDED(hr))
        {
            // Use IEnumTuningSpaces to iterate through the collection.
        }
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

