---
UID: NN:oleidl.IParseDisplayName
title: IParseDisplayName
author: windows-sdk-content
description: Parses a displayable name string to convert it into a moniker for custom moniker implementations.
old-location: com\iparsedisplayname.htm
tech.root: com
ms.assetid: 37844d9b-35ce-4d30-8a58-dac4c671896f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IParseDisplayName, IParseDisplayName interface [COM], IParseDisplayName interface [COM],described, _com_iparsedisplayname, com.iparsedisplayname, oleidl/IParseDisplayName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - OleIdl.h
api_name:
 - IParseDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IParseDisplayName</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IParseDisplayName</b> also has these types of members:
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



<a href="https://msdn.microsoft.com/library/ms775113(v=VS.85).aspx">MkParseDisplayNameEx</a>
 

 

