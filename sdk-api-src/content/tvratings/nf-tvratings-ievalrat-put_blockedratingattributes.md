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

# IEvalRat::put_BlockedRatingAttributes


## -description


The <b>put_BlockedRatingAttributes</b> method specifies whether to block content that has a specified rating.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param enLevel [in]

Specifies the rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.


### -param lbfAttrs [in]

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration. The flags specify whether the overall rating is blocked, or specific attributes within the rating are blocked.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method should be called once for each level in a rating system, to specify viewing permissions for that level. The <i>lbfAttrs</i> parameter indicates the permissions for the specified rating level:

<ul>
<li>If no flags are set, this rating level is unrestricted. Any program with this rating level can be viewed.</li>
<li>If the <b>BflsBlocked</b> flag is set, this rating level is restricted. No program with this rating level can be viewed.</li>
<li>Flags in the range <b>BfIsAttr_1</b> to <b>BfIsAttr_7</b> specify content attributes, such as violence or adult language. If one of these flags is set, it means that a program with that content attribute and the specified rating level will be blocked.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat Interface</a>
 

 

