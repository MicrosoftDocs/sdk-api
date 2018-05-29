---
UID: NN:bdaiface.IFrequencyMap
title: IFrequencyMap
author: windows-sdk-content
description: The IFrequencyMap interface sets the frequency table used by the BDA Network Provider filter.A frequency table is a list of broadcast or cable frequencies for a given country/region.
old-location: mstv\ifrequencymap.htm
old-project: mstv
ms.assetid: 0f7f1b2c-a191-45f5-a645-367e898b6ee2
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFrequencyMap, IFrequencyMap interface [Microsoft TV Technologies], IFrequencyMap interface [Microsoft TV Technologies],described, IFrequencyMapInterface, bdaiface/IFrequencyMap, mstv.ifrequencymap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IFrequencyMap
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFrequencyMap interface


## -description



The <b>IFrequencyMap</b> interface sets the frequency table used by the <a href="https://msdn.microsoft.com/f5de924f-defe-4300-a347-c9d63271dc90">BDA Network Provider</a> filter.

A frequency table is a list of broadcast or cable frequencies for a given country/region. The Network Provider uses a frequency table to find the next frequency when <a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner</a> methods are called. On startup, the Network Provider loads a default frequency table. An application can use the <b>IFrequencyMap</b> interface to specify the user's country/region, which causes the Network Provider filter to load the corresponding frequency table. The application can also modify the current table, or provide a completely new table, using the <a href="https://msdn.microsoft.com/cfde2c8e-803d-46b8-b3d4-8e9b3129af0e">put_FrequencyMapping</a> method.

Frequencies used by this interface are measured in units of kilohertz (kHz), and refer to the center frequency of each band. For more information, see "Terrestrial delivery system descriptor" in the ETSI EN 300 468 standard.

<div class="alert"><b>Note</b>  Currently only the DVB-T Network Provider supports this interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFrequencyMap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFrequencyMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFrequencyMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f5e4109-e424-40be-9b3c-7eeef895e677">get_CountryCode</a>
</td>
<td align="left" width="63%">
Returns the country/region code that the Network Provider is currently using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc9e2f2e-3187-446e-b1e6-ae32da4413b9">get_CountryCodeList</a>
</td>
<td align="left" width="63%">
Returns a list of all the country/region codes for which the Network Provider has a frequency table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67057c70-cb4d-4828-ad97-cf0181bd8cfe">get_DefaultFrequencyMapping</a>
</td>
<td align="left" width="63%">
Returns the default frequency table for a given country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51fe636f-febe-4306-9c9a-7031a85440c6">get_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Returns the Network Provider filter's current frequency table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8473e292-b47b-4c1a-b45e-b8acf0e36263">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfde2c8e-803d-46b8-b3d4-8e9b3129af0e">put_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Sets the frequency table.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IFrequencyMap)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

