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

# ITfComposition::EndComposition


## -description




## -parameters




### -param ecWrite [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This value results when:

<ul>
<li>The composition terminated.</li>
<li>The caller is inside another composition write operation.</li>
<li>The caller does not own the composition.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ecWrite</i> does not have a read/write lock.

</td>
</tr>
</table>
 




## -remarks



This method does not release the composition object, but the <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition</a> methods will fail with E_UNEXPECTED after this method is called.

Context owners should use the <a href="https://msdn.microsoft.com/950ba2b3-cb12-4697-a4b2-1c87373b9a23">ITFContextOwnerCompositionServices::TerminateComposition</a> method to terminate a composition.

This method causes the GUID_PROP_COMPOSING property to be removed from the text covered by the composition.




## -see-also




<a href="https://msdn.microsoft.com/950ba2b3-cb12-4697-a4b2-1c87373b9a23">
        ITFContextOwnerCompositionServices::TerminateComposition
      </a>



<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">
        ITfComposition
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>
 

 

