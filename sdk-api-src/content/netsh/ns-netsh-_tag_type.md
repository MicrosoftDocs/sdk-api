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

# _TAG_TYPE structure


## -description


The 
<b>TAG_TYPE</b> structure specifies tags used for the 
<a href="https://msdn.microsoft.com/6795512e-4b90-47da-962a-d9e6ecfb7ee0">PreprocessCommand</a> function.


## -struct-fields




### -field pwszTag

A tag string, in UNICODE.


### -field dwRequired

 


### -field bPresent

This value specifies whether the tag is present. <b>TRUE</b> indicates the tag is present.


#### - Required

Specifies whether the tag is required.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ZERO"></a><a id="ns_req_zero"></a><dl>
<dt><b>NS_REQ_ZERO</b></dt>
</dl>
</td>
<td width="60%">
Tag is optional.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_PRESENT"></a><a id="ns_req_present"></a><dl>
<dt><b>NS_REQ_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
Tag must be present.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ALLOW_MULTIPLE"></a><a id="ns_req_allow_multiple"></a><dl>
<dt><b>NS_REQ_ALLOW_MULTIPLE</b></dt>
</dl>
</td>
<td width="60%">
Multiple copies of the tag is allowed.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_REQ_ONE_OR_MORE"></a><a id="ns_req_one_or_more"></a><dl>
<dt><b>NS_REQ_ONE_OR_MORE</b></dt>
</dl>
</td>
<td width="60%">
Multiple copies of the tag is allowed. Tag must be present.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/6795512e-4b90-47da-962a-d9e6ecfb7ee0">PreprocessCommand</a>
 

 

