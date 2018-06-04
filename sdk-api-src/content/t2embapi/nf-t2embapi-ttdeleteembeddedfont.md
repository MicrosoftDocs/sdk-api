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

# TTDeleteEmbeddedFont function


## -description


Releases memory used by an embedded font, <i>hFontReference</i>.

By default, <b>TTDeleteEmbeddedFont</b> also removes the installed version of the font from the user's system. When an installable font is loaded, this function still must be called to release the memory used by the embedded font structure, but a flag can be specified indicating that the font should remain installed on the system.


## -parameters




### -param hFontReference [in]

Handle identifying font, as provided in the <a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a> function.


### -param ulFlags [in]

Flag specifying font deletion options. Currently, this flag can be set to zero or the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TTDELETE_DONTREMOVEFONT"></a><a id="ttdelete_dontremovefont"></a><dl>
<dt><b>TTDELETE_DONTREMOVEFONT</b></dt>
</dl>
</td>
<td width="60%">
Do not remove the installed font from the system, but release the memory previously occupied by the embedded font structure.

</td>
</tr>
</table>
 


### -param pulStatus [out]

Currently undefined.


## -returns



If successful, <b>TTDeleteEmbeddedFont</b> returns a value of E_NONE.

The memory occupied by the embedded font structure is cleared. By default, the font indicated by <i>hFontReference</i> is also permanently removed (uninstalled and deleted) from the system.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding-Function Error Messages</a>.




## -remarks



The client is responsible for calling this function to remove fonts when the embedding privileges do not allow a font to be permanently installed on a user's system.




## -see-also




<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 

