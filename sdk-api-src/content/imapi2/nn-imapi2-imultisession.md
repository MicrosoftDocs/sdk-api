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

# IMultisession interface


## -description


Base interface containing properties common to derived multisession interfaces.

You can derive from this interface to implement a new multi-session mechanism that is different from <a href="https://msdn.microsoft.com/b8124597-e75a-4f95-a25c-8cf59f452548">IMultisessionSequential</a> and <a href="https://msdn.microsoft.com/1843254d-7947-4197-9c1b-6dc01abe9354">IMultisessionRandomWrite</a>. For example, you could implement a mechanism for BD-R Pseudo-Overwrite. 

To access media-specific properties of a multisession interface, use the <a href="https://msdn.microsoft.com/b8124597-e75a-4f95-a25c-8cf59f452548">IMultisessionSequential</a> and <a href="https://msdn.microsoft.com/1843254d-7947-4197-9c1b-6dc01abe9354">IMultisessionRandomWrite</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultisession</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMultisession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultisession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eca127eb-0e0a-4f43-afa4-42fde8d43284">get_ImportRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the disc recorder to use to import one or more previous sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35ebf336-0d67-422c-b6f7-2fd6ee3e7226">get_InUse</a>
</td>
<td align="left" width="63%">
Determines if this multi-session type is the one you should use on the current media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cabfa0a2-15db-4ef4-b852-b6306d2b49a1">get_IsSupportedOnCurrentMediaState</a>
</td>
<td align="left" width="63%">
Determines if the multi-session type can write to the current optical media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4eef9de-8b7e-4326-b66f-dddbe2b8a05d">put_InUse</a>
</td>
<td align="left" width="63%">
Determines if this multi-session type is the one you should use on the current media.

</td>
</tr>
</table> 


## -remarks



If more than one multi-session interface exist, the application can let <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> choose a compatible multi-session interface to use  or the application can specify the multi-session interface to use by setting the <a href="https://msdn.microsoft.com/d4eef9de-8b7e-4326-b66f-dddbe2b8a05d">put_InUse</a> property to VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

