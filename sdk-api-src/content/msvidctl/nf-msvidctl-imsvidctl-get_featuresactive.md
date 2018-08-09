---
UID: NF:msvidctl.IMSVidCtl.get_FeaturesActive
title: IMSVidCtl::get_FeaturesActive
author: windows-sdk-content
description: The get_FeaturesActive method retrieves the features that are currently active.
old-location: mstv\imsvidctl_get_featuresactive.htm
old-project: mstv
ms.assetid: 33832fe2-e8ef-4e37-9af9-90f566feb559
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_FeaturesActive method, IMSVidCtl.get_FeaturesActive, IMSVidCtl::get_FeaturesActive, IMSVidCtlget_FeaturesActive, get_FeaturesActive, get_FeaturesActive method [Microsoft TV Technologies], get_FeaturesActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_featuresactive, msvidctl/IMSVidCtl::get_FeaturesActive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_FeaturesActive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidCtl::get_FeaturesActive


## -description


The <b>get_FeaturesActive</b> method retrieves the features that are currently active.


## -parameters




### -param pVal






#### - ppVal [out]

Receives an <a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures</a> interface pointer. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If no features are active, the method might return <b>NULL</b> in the <i>pVal</i> parameter. Otherwise, it returns a collection of feature objects. Use the returned <a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures</a> pointer to enumerate the collection.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt;IMSVidFeatures&gt; pFeatures;
hr = m_pVideoControl-&gt;get_FeaturesActive(&amp;pFeatures);
if (SUCCEEDED(hr) &amp;&amp; pFeatures)
{
    long c;
    pFs-&gt;get_Count(&amp;c);
    /* Enumerate the features */
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/699f4021-1c9c-4855-8295-5b84bc512252">Displaying Closed Captioning in C++</a>



<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/293506fa-3208-468e-982a-3c1f8ce0269b">IMSVidCtl::put_FeaturesActive</a>
 

 

