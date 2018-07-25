---
UID: NN:tapi3if.ITMediaRecord
title: ITMediaRecord
author: windows-sdk-content
description: The ITMediaRecord interface provides recording-specific methods that allow an application to set and get the names of files to record.
old-location: tapi3\itmediarecord.htm
old-project: tapi
ms.assetid: 604b0128-1461-40f2-98fe-801dbb71e005
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITMediaRecord, ITMediaRecord interface [TAPI 2.2], ITMediaRecord interface [TAPI 2.2],described, _tapi3_itmediarecord, tapi3.itmediarecord, tapi3if/ITMediaRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaRecord
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMediaRecord interface


## -description


The 
<b>ITMediaRecord</b> interface provides recording-specific methods that allow an application to set and get the names of files to record.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITMediaRecord</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITMediaRecord</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITMediaRecord</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd97665c-ff9e-4621-baf9-7c0b603400c5">get_FileName</a>
</td>
<td align="left" width="63%">
Gets the name of the file used for recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3f6155d-3989-49d7-8944-da26fd03617a">put_FileName</a>
</td>
<td align="left" width="63%">
Sets the name of the file to record.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/66b43721-f902-4a0e-8cbb-418438617f47">ITMediaPlayback</a>
 

 

