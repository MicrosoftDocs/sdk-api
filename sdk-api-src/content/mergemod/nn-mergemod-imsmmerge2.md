---
UID: NN:mergemod.IMsmMerge2
title: IMsmMerge2 (mergemod.h)
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.The IMsmMerge2 interface provides a way for the client merge tool to utilize the new configurable-module functionality.
helpviewer_keywords: ["IMsmMerge2","IMsmMerge2 interface","IMsmMerge2 interface","described","_msi_imsmmerge2_interface","mergemod/IMsmMerge2","setup.imsmmerge2_interface"]
old-location: setup\imsmmerge2_interface.htm
tech.root: Msi
ms.assetid: cda5698d-4aee-4771-9989-628162b433ef
ms.date: 12/05/2018
ms.keywords: IMsmMerge2, IMsmMerge2 interface, IMsmMerge2 interface,described, _msi_imsmmerge2_interface, mergemod/IMsmMerge2, setup.imsmmerge2_interface
f1_keywords:
- mergemod/IMsmMerge2
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmMerge2 interface


## -description


The 
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nn-mergemod-imsmmerge">IMsmMerge</a> interface and the 
<b>IMsmMerge2</b> interface provide interfaces to the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-object">Merge object</a>.The 
<b>IMsmMerge2</b> interface provides a way for the client merge tool to utilize the new configurable-module functionality. Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID. This CLSID supports existing functionality available through the 
<b>IMsmMerge</b> interface, but the default interface on the object (and the associated dual interface) is the 
<b>IMsmMerge2</b> interface instead of the 
<b>IMsmMerge</b> interface.

Requesting this interface does not commit the tool to using the new functionality. The interface supports both the standard and the "Ex" versions of the appropriate interface calls.

The 
<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-object">Merge</a> object provides access to other top-level objects. A 
Merge object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmMerge2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closedatabase">CloseDatabase</a>
</td>
<td align="left" width="63%">
Closes the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closelog">CloseLog</a>
</td>
<td align="left" width="63%">
Closes the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closemodule">CloseModule</a>
</td>
<td align="left" width="63%">
Closes the current module

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects the components in a module to the specified feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge2-createsourceimage">CreateSourceImage</a>
</td>
<td align="left" width="63%">
Extracts files from a module to a source image on disk after a merge, with configuration changes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-extractcab">ExtractCAB</a>
</td>
<td align="left" width="63%">
Extracts the embedded CAB of a Merge Module to a disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-extractfiles">ExtractFiles</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge2-extractfilesex">ExtractFilesEx</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge2-get_configurableitems">get_ConfigurableItems</a>
</td>
<td align="left" width="63%">
Returns a collection of configurable items in the database. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-get_dependencies">get_Dependencies</a>
</td>
<td align="left" width="63%">
Returns a collection of all unsatisfied dependencies in the database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-get_errors">get_Errors</a>
</td>
<td align="left" width="63%">
Returns a collection of all errors from the most recent merge operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-log">Log</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-merge">Merge</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge2-mergeex">MergeEx</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-opendatabase">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens a database to use as the merge target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-openlog">OpenLog</a>
</td>
<td align="left" width="63%">
Opens a log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-openmodule">OpenModule</a>
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

<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-configurableitems">ConfigurableItems</a>


</td>
<td align="left" width="63%">
Returns a collection of configurable items in the database. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-dependencies">Dependencies</a>


</td>
<td align="left" width="63%">
Returns a collection of all unsatisfied dependencies in the database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-errors">Errors</a>


</td>
<td align="left" width="63%">
Returns a collection of all errors from the most recent merge operation.

</td>
</tr>
</table> 

