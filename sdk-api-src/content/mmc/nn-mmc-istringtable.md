---
UID: NN:mmc.IStringTable
title: IStringTable
author: windows-sdk-content
description: The IStringTable interface is introduced in MMC 1.1.
old-location: mmc\istringtable.htm
tech.root: mmc
ms.assetid: 3b4cfc92-4f50-4b62-bb2c-77c8e0e003da
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: IStringTable, IStringTable interface [MMC], IStringTable interface [MMC],described, _slate_istringtable, mmc.istringtable, mmc/IStringTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IStringTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStringTable interface


## -description


The 
<b>IStringTable</b> interface is introduced in MMC 1.1.

The 
<b>IStringTable</b> interface provides a way to store string data with the snap-in. A string table is created in the console file as required for each snap-in by MMC.

The 
<b>IStringTable</b> interface allows strings to be saved in the console file. Be aware that this interface is designed to work with specialized localization tools. Snap-ins without access to these localization tools will not benefit from using this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringTable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStringTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStringTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd4672fb-89d1-4542-b917-58c01290c928">AddString</a>
</td>
<td align="left" width="63%">
Adds a string to the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a0b02f6-3c15-4687-a1b8-2beba40dd1dc">DeleteAllStrings</a>
</td>
<td align="left" width="63%">
Removes all string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57d04890-5dd8-45e5-9b46-b982ea3a4f36">DeleteString</a>
</td>
<td align="left" width="63%">
Removes a string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d23e29d-a80f-4710-8285-c9e64fd580a1">Enumerate</a>
</td>
<td align="left" width="63%">
Returns an enumerator into a snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c239618d-ed27-4d73-9e88-7323960a0e68">FindString</a>
</td>
<td align="left" width="63%">
Finds a string in the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34dbf92a-b54d-4f60-87ff-493c9946a57d">GetString</a>
</td>
<td align="left" width="63%">
Retrieves a string from the snap-in string table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1924c4fa-ecbb-4f03-8c93-e2bb3dc8f4e3">GetStringLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of a string from the snap-in string table.

</td>
</tr>
</table> 

