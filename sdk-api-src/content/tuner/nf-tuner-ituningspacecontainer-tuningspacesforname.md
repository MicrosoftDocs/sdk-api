---
UID: NF:tuner.ITuningSpaceContainer.TuningSpacesForName
title: ITuningSpaceContainer::TuningSpacesForName
author: windows-driver-content
description: The TuningSpacesForName method retrieves a collection of tuning spaces that match the specified name.
old-location: mstv\ituningspacecontainer_tuningspacesforname.htm
old-project: mstv
ms.assetid: de16a50e-7f5d-41e5-a17f-bb6d97179e4e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],TuningSpacesForName method, ITuningSpaceContainer.TuningSpacesForName, ITuningSpaceContainer::TuningSpacesForName, ITuningSpaceContainerTuningSpacesForName, TuningSpacesForName, TuningSpacesForName method [Microsoft TV Technologies], TuningSpacesForName method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_tuningspacesforname, tuner/ITuningSpaceContainer::TuningSpacesForName
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpaceContainer.TuningSpacesForName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

