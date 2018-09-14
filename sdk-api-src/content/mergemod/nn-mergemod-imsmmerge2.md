---
UID: NN:mergemod.IMsmMerge2
title: IMsmMerge2
author: windows-sdk-content
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.The IMsmMerge2 interface provides a way for the client merge tool to utilize the new configurable-module functionality.
old-location: setup\imsmmerge2_interface.htm
tech.root: msi
ms.assetid: cda5698d-4aee-4771-9989-628162b433ef
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IMsmMerge2, IMsmMerge2 interface, IMsmMerge2 interface,described, _msi_imsmmerge2_interface, mergemod/IMsmMerge2, setup.imsmmerge2_interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
 - IMsmMerge2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmMerge2 interface


## -description


The 
<a href="https://msdn.microsoft.com/6cb4b620-88ce-4348-ab72-6d2ed60c6298">IMsmMerge</a> interface and the 
<b>IMsmMerge2</b> interface provide interfaces to the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge object</a>.The 
<b>IMsmMerge2</b> interface provides a way for the client merge tool to utilize the new configurable-module functionality. Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID. This CLSID supports existing functionality available through the 
<b>IMsmMerge</b> interface, but the default interface on the object (and the associated dual interface) is the 
<b>IMsmMerge2</b> interface instead of the 
<b>IMsmMerge</b> interface.

Requesting this interface does not commit the tool to using the new functionality. The interface supports both the standard and the "Ex" versions of the appropriate interface calls.

The 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object provides access to other top-level objects. A 
Merge object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMsmMerge2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMsmMerge2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efbb6238-e9e3-4603-896a-75fcff2bb362">CloseDatabase</a>
</td>
<td align="left" width="63%">
Closes the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f683e405-da98-455f-85d5-d61dc1d73440">CloseLog</a>
</td>
<td align="left" width="63%">
Closes the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe8ab14-3d8e-441c-a9bf-0319a9b3a5de">CloseModule</a>
</td>
<td align="left" width="63%">
Closes the current module

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f491beb8-90f7-4e41-891d-ef674306339d">Connect</a>
</td>
<td align="left" width="63%">
Connects the components in a module to the specified feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42fa644-f0e6-4261-af76-741df572df3a">CreateSourceImage</a>
</td>
<td align="left" width="63%">
Extracts files from a module to a source image on disk after a merge, with configuration changes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f794dac-6eeb-4c1e-8c23-c9d7384f650f">ExtractCAB</a>
</td>
<td align="left" width="63%">
Extracts the embedded CAB of a Merge Module to a disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5bafd2d-0750-4aa6-87e8-22ef3cfdd5ff">ExtractFiles</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba6adc9-a08f-47a6-b8a8-1624bd856511">ExtractFilesEx</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8b34ff7-6b0b-4cd9-bcb2-9d0da6b14254">get_ConfigurableItems</a>
</td>
<td align="left" width="63%">
Returns a collection of configurable items in the database. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e59ac31-647e-4dd2-8f56-993eb4c59ab2">get_Dependencies</a>
</td>
<td align="left" width="63%">
Returns a collection of all unsatisfied dependencies in the database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81bf84f6-d469-47b1-9097-8a3ee9c8550d">get_Errors</a>
</td>
<td align="left" width="63%">
Returns a collection of all errors from the most recent merge operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15c7450b-6887-4a54-8f4f-ac2cf5944f17">Log</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ff1a2a8-accb-43d7-ba38-a89a5d099dc5">Merge</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdfd950f-cba9-4b87-ae07-c3d3b127f69d">MergeEx</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cafe02a0-2e86-43f6-9cde-e3dd23bdfc4c">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens a database to use as the merge target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b34e7f28-2cf3-4cc7-9a39-e1da6fb8c788">OpenLog</a>
</td>
<td align="left" width="63%">
Opens a log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37225e61-c24f-4a44-8fdf-673590a6e09d">OpenModule</a>
</td>
<td align="left" width="63%">
Opens a merge module for use as the merge source.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4d1a64f7-fbd0-4358-8911-112e43f1be4a">ConfigurableItems</a>


</td>
<td align="left" width="63%">
Returns a collection of configurable items in the database. 

</td>
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

