---
UID: NN:tapi3if.ITCallInfo2
title: ITCallInfo2
author: windows-sdk-content
description: The ITCallInfo2 interface is an extension of the ITCallInfo interface. ITCallInfo2 provides additional methods that allow an application to set event filtering on a per-call basis.
old-location: tapi3\itcallinfo2.htm
tech.root: tapi
ms.assetid: 20f7b20e-37f8-49f7-ae9d-83a9b9f574b6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITCallInfo2, ITCallInfo2 interface [TAPI 2.2], ITCallInfo2 interface [TAPI 2.2],described, _tapi3_itcallinfo2, tapi3.itcallinfo2, tapi3if/ITCallInfo2
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo2 interface


## -description


The 
<b>ITCallInfo2</b> interface is an extension of the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface. 
<b>ITCallInfo2</b> provides additional methods that allow an application to set event filtering on a per-call basis.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallInfo2</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITCallInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21f4f7ae-2bba-424b-889f-4b43e9416b33">get_EventFilter</a>
</td>
<td align="left" width="63%">
Gets the current status of a filtering for a given event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e1b4474-b9ff-489d-8226-58eda659e057">put_EventFilter</a>
</td>
<td align="left" width="63%">
Sets filtering for a given event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

