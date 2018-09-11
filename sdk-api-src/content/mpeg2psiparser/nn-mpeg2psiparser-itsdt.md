---
UID: NN:mpeg2psiparser.ITSDT
title: ITSDT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itsdt.htm
tech.root: mstv
ms.assetid: 58ec73dc-79bd-415b-b9be-8e9246166391
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITSDT, ITSDT interface [Microsoft TV Technologies], ITSDT interface [Microsoft TV Technologies],described, ITSDTInterface, mpeg2psiparser/ITSDT, mstv.itsdt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mpeg2psiparser.h
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
 - Mpeg2PsiParser.h
api_name:
 - ITSDT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSDT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>ITSDT</b> interface enables the client to get data from a transport stream description table (TSDT). The <a href="https://msdn.microsoft.com/f9c25b9e-615d-4223-baf5-f4df2fc1473a">IAtscPsipParser::GetTSDT</a> and <a href="https://msdn.microsoft.com/1aae16d0-6852-476b-85a6-6a994400b651">IDvbSiParser::GetTSDT</a> methods return pointers to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSDT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ce79ed-516a-44bf-b9c9-ff6d693cdd30">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29e2f3f7-4ff4-447b-bd17-36cd05829844">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the TSDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b60647a-b668-4884-967d-044ff0d149c2">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9adcc8f6-44a7-41c6-b42a-e45c33cd5d6a">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table descriptor for the TSDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb2f544b-02fd-4a48-838f-56815710a5bd">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the TSDT for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4784b7d6-1a20-4018-9ad5-7e8bafb700f8">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the TSDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6682de14-50a8-48be-839f-b15824c1dd6e">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36d597e2-0a65-48f3-8220-bb3481185af7">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2ce7908-3650-4ecf-8014-6bae377dcb5c">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

