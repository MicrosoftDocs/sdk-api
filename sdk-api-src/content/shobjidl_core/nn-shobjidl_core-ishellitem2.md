---
UID: NN:shobjidl_core.IShellItem2
title: IShellItem2
author: windows-sdk-content
description: Extends IShellItem with methods that retrieve various property values of the item. IShellItem and IShellItem2 are the preferred representations of items in any new code.
old-location: shell\IShellItem2.htm
tech.root: shell
ms.assetid: e54d8385-ec67-4825-ad7c-431807a4fcb4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IShellItem2, IShellItem2 interface [Windows Shell], IShellItem2 interface [Windows Shell],described, _shell_IShellItem2, shell.IShellItem2, shobjidl_core/IShellItem2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IShellItem2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItem2 interface


## -description


Extends <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> with methods that retrieve various property values of the item. <b>IShellItem</b> and <b>IShellItem2</b> are the preferred representations of items in any new code.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItem2</b> interface inherits from <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>. <b>IShellItem2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItem2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/754d0a7a-a6b4-41ef-8c8f-483539f7d53e">GetBool</a>
</td>
<td align="left" width="63%">
Gets the boolean value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95b0c5fb-db09-4db0-8253-708f2dc2944b">GetCLSID</a>
</td>
<td align="left" width="63%">
Gets the CLSID value of specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdd1834d-ce00-45e2-8fe7-825e18e12b96">GetFileTime</a>
</td>
<td align="left" width="63%">
Gets the date and time value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b56036e-316b-4300-979c-151422f74bd2">GetInt32</a>
</td>
<td align="left" width="63%">
Gets the Int32 value of specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72e23b9-e99b-462b-91b6-9ef27a4fc9e1">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure from a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/443b95c9-0a9e-4ad5-8774-ad3b1b51c136">GetPropertyDescriptionList</a>
</td>
<td align="left" width="63%">
Gets a property description list object given a reference to a property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">GetPropertyStore</a>
</td>
<td align="left" width="63%">
Gets a property store object for specified property store flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d32ece8-4a68-4bf2-a1ee-bd94a2aa6fbd">GetPropertyStoreForKeys</a>
</td>
<td align="left" width="63%">
Gets property store object for specified property keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a90ea62-e4d7-4876-802a-9c1f6c296714">GetPropertyStoreWithCreateObject</a>
</td>
<td align="left" width="63%">
Uses the specified <a href="https://msdn.microsoft.com/90502b4a-dc0a-4077-83d7-e9f5445ba69b">ICreateObject</a> instead of <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create an instance of the property handler associated with the Shell item on which this method is called. Most calling applications do not need to call this method, and can call <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a> instead.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/912b3653-340b-4186-b652-53d958534c1d">GetString</a>
</td>
<td align="left" width="63%">
Gets the string value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f9b479f-974f-4fad-87ea-7335d4d5d2e3">GetUInt32</a>
</td>
<td align="left" width="63%">
Gets the UInt32 value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c8a180f-336f-4887-b04b-dbe8f34d4302">GetUInt64</a>
</td>
<td align="left" width="63%">
Gets the UInt64 value of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42000a83-2ee0-49b9-b3fc-328685e25c0b">Update</a>
</td>
<td align="left" width="63%">
Ensures that any cached information in this item is updated.

</td>
</tr>
</table> 

