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

# IParseDisplayName interface


## -description


Parses a displayable name string to convert it into a moniker for custom moniker implementations.

Display name parsing is necessary when the end user inputs a string to identify a component, as in the following situations: 

<ul>
<li>A compound document application that supports linked components typically supports the <b>Edit:Links...</b> dialog box. Through this dialog box, the end user can enter a display name to specify a new link source for a specified linked component. The compound document needs to have this input string converted into a moniker.</li>
<li>A script language such as the macro language of a spreadsheet can allow textual references to a component. The language's interpreter needs to have such a reference converted into a moniker in order to execute the macro.</li>
</ul>This interface is not supported for use across machine boundaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IParseDisplayName</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IParseDisplayName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IParseDisplayName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf18320c-1ff3-4280-bd67-70f6c2998285">ParseDisplayName</a>
</td>
<td align="left" width="63%">
Parses the specified display name and creates a corresponding moniker.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6a5a1f14-f14f-404b-90d8-0afceafc087c">IMoniker::ParseDisplayName</a>



<a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a>



<a href="https://msdn.microsoft.com/ada46dd3-e2c5-4ff5-89bd-3805f98b247b">MkParseDisplayName</a>



<a href="_inet_MkParseDisplayNameEx_Function_cpp">MkParseDisplayNameEx</a>
 

 

