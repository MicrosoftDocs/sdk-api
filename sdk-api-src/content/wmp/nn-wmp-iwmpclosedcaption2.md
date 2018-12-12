---
UID: NN:wmp.IWMPClosedCaption2
title: IWMPClosedCaption2
author: windows-sdk-content
description: The IWMPClosedCaption2 interface provides closed captioning methods that supplement the IWMPClosedCaption interface.
old-location: wmp\iwmpclosedcaption2.htm
tech.root: WMP
ms.assetid: 21067ac1-d29e-4f1b-b123-34b24929369a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPClosedCaption2, IWMPClosedCaption2 interface [Windows Media Player], IWMPClosedCaption2 interface [Windows Media Player],described, IWMPClosedCaption2Interface, wmp.iwmpclosedcaption2, wmp/IWMPClosedCaption2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPClosedCaption2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPClosedCaption2 interface


## -description



The <b>IWMPClosedCaption2</b> interface provides closed captioning methods that supplement the <b>IWMPClosedCaption</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPClosedCaption2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd563113(v=VS.85).aspx">IWMPClosedCaption</a>. <b>IWMPClosedCaption2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPClosedCaption2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563118(v=VS.85).aspx">get_SAMILangCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of languages supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563119(v=VS.85).aspx">get_SAMIStyleCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of styles supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563115(v=VS.85).aspx">getSAMILangID</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563116(v=VS.85).aspx">getSAMILangName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563117(v=VS.85).aspx">getSAMIStyleName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a style supported by the current SAMI file.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPClosedCaption2</b> interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/en-us/library/Dd563113(v=VS.85).aspx">IWMPClosedCaption</a> interface.

	


## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563113(v=VS.85).aspx">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

