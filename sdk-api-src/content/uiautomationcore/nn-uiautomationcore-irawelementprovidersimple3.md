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

# IRawElementProviderSimple3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7">IRawElementProviderSimple2</a> interface to enable retrieving metadata about how accessible technology should say the preferred content type.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderSimple3</b> interface inherits from <a href="https://msdn.microsoft.com/0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7">IRawElementProviderSimple2</a>. <b>IRawElementProviderSimple3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderSimple3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/832154F3-22D3-48E9-BC4E-CB495BB72485">GetMetadataValue</a>
</td>
<td align="left" width="63%">
Gets metadata from the UI Automation element that indicates how the information should be interpreted.

</td>
</tr>
</table> 


## -remarks



Screen reading accessibility tools like Narrator use a speech synthesizer to read what an app is showing.  Speech synthesizers usually read the provided content well based on the content description.

However, the speech synthesizer could use some help describing the preferred content type. The SayAs command provides accurate content reading from a Microsoft UI Automation provider to a UI Automation client (such as a screen reader) through UI Automation core APIs.

Examples:

<ul>
<li>Given the date 10/4, is the format Month/Day or Day/Month?
If a screen reader does not know, you could hear October 4th or 10th April. 
</li>
<li>
Given the string "10-100", is this
"Ten to one hundred" or
"Ten minus 100"?

The ability to mark the "10" as a number and the "-100" as a number helps active technology (AT) read it better.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7">IRawElementProviderSimple2</a>
 

 

