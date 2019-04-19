---
UID: NN:wabdefs.IABContainer
title: IABContainer (wabdefs.h)
author: windows-sdk-content
description: Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.
old-location: wab\_wab_IABContainer.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iabcontainer\iabcontainer.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IABContainer, IABContainer interface [Windows Address Book], IABContainer interface [Windows Address Book],described, _wab_IABContainer, wab._wab_IABContainer, wabdefs/IABContainer
ms.topic: interface
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IABContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# IABContainer interface


## -description


Do not use. This interface provides access to address book containers. Applications call the methods of the interface to perform name resolution and to create, copy, and delete recipients.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IABContainer</b> interface inherits from <a href="https://msdn.microsoft.com/library/Cc839817(v=office.12).aspx">IMAPIContainer</a>. <b>IABContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IABContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629670(v=VS.85).aspx">CopyEntries</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629671(v=VS.85).aspx">CopyProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629674(v=VS.85).aspx">CopyTo</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629676(v=VS.85).aspx">CreateEntry</a>
</td>
<td align="left" width="63%">
Creates a new entry in the address book container.  The WAB supports creation of mail users and distribution lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629678(v=VS.85).aspx">DeleteEntries</a>
</td>
<td align="left" width="63%">
Removes one or more entries from the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629680(v=VS.85).aspx">DeleteProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629682(v=VS.85).aspx">GetContentsTable</a>
</td>
<td align="left" width="63%">
Retrieves the address of the contents table of the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629684(v=VS.85).aspx">GetHierarchyTable</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629687(v=VS.85).aspx">GetIDsFromNames</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629690(v=VS.85).aspx">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629692(v=VS.85).aspx">GetNamesFromIDs</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629694(v=VS.85).aspx">GetPropList</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629696(v=VS.85).aspx">GetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629698(v=VS.85).aspx">GetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629702(v=VS.85).aspx">OpenEntry</a>
</td>
<td align="left" width="63%">
Opens a child container object in the open container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629704(v=VS.85).aspx">OpenProperty</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629706(v=VS.85).aspx">ResolveNames</a>
</td>
<td align="left" width="63%">
Resolves entries against the address book container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629708(v=VS.85).aspx">SaveChanges</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629710(v=VS.85).aspx">SetProps</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629712(v=VS.85).aspx">SetSearchCriteria</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 

