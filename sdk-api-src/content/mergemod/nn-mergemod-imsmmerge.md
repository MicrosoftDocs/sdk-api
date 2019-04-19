---
UID: NN:mergemod.IMsmMerge
title: IMsmMerge (mergemod.h)
author: windows-sdk-content
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.
old-location: setup\imsmmerge_interface.htm
tech.root: Msi
ms.assetid: 6cb4b620-88ce-4348-ab72-6d2ed60c6298
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMsmMerge, IMsmMerge interface, IMsmMerge interface,described, _msi_imsmmerge_interface, mergemod/IMsmMerge, setup.imsmmerge_interface
ms.topic: interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmMerge interface


## -description


The 
<b>IMsmMerge</b> interface and the 
<a href="https://msdn.microsoft.com/cda5698d-4aee-4771-9989-628162b433ef">IMsmMerge2</a> interface provide interfaces to the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object. The 
Merge object provides access to other top-level objects. A 
<b>Merge</b> object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMsmMerge</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMsmMerge</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a89fe77a-0099-4c49-b484-c05ee351a66a">CloseDatabase method</a>
</td>
<td align="left" width="63%">
Closes the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09a40de4-d92f-4fc8-8556-a50f5dbe856b">CloseLog</a>
</td>
<td align="left" width="63%">
Closes the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a11f72cf-4c4e-4650-95f9-549169452622">CloseModule</a>
</td>
<td align="left" width="63%">
Closes the current module

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c1ef664-792c-4cdc-b468-1ffe0b7810a5">Connect</a>
</td>
<td align="left" width="63%">
Connects the components in a module to the specified feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6fe8b69-8f4a-45f7-b7e6-7620a00500bb">ExtractCAB</a>
</td>
<td align="left" width="63%">
Extracts the embedded CAB of a Merge Module to a disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa369815(v=VS.85).aspx">ExtractFiles</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbfc9be7-1b0b-417e-9e2b-bf191ea255b6">Log</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b580b1f-5071-42f1-8022-a152817f9fdc">Merge</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86f168e5-bc76-476d-9757-9b2a21bb9c4b">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens a database to use as the merge target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97d01ea3-43b6-4529-9706-97b3b0132d9c">OpenLog</a>
</td>
<td align="left" width="63%">
Opens a log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc976899-2c39-4314-b2fb-417e0dfc53b9">OpenModule</a>
</td>
<td align="left" width="63%">
Opens a merge module for use as the merge source.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d7081ffe-3d9e-486e-84b6-b45e92fff5f0">Dependencies</a>


</td>
<td align="left" width="63%">
Returns a collection of all unsatisfied dependencies in the database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/619f17cc-131a-4262-ad48-9ab1318142aa">Errors</a>


</td>
<td align="left" width="63%">
Returns a collection of all errors from the most recent merge operation.

</td>
</tr>
</table> 

