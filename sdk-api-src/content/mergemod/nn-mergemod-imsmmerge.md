---
UID: NN:mergemod.IMsmMerge
title: IMsmMerge (mergemod.h)
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.
helpviewer_keywords: ["IMsmMerge","IMsmMerge interface","IMsmMerge interface","described","_msi_imsmmerge_interface","mergemod/IMsmMerge","setup.imsmmerge_interface"]
old-location: setup\imsmmerge_interface.htm
tech.root: setup
ms.assetid: 6cb4b620-88ce-4348-ab72-6d2ed60c6298
ms.date: 12/05/2018
ms.keywords: IMsmMerge, IMsmMerge interface, IMsmMerge interface,described, _msi_imsmmerge_interface, mergemod/IMsmMerge, setup.imsmmerge_interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge
 - mergemod/IMsmMerge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge
---

# IMsmMerge interface


## -description

The 
<b>IMsmMerge</b> interface and the 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge2">IMsmMerge2</a> interface provide interfaces to the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. The 
Merge object provides access to other top-level objects. A 
<b>Merge</b> object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmMerge</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmMerge</b> also has these types of members:
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
<a href="/windows/desktop/Msi/merge-closedatabase">CloseDatabase method</a>
</td>
<td align="left" width="63%">
Closes the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-closelog">CloseLog</a>
</td>
<td align="left" width="63%">
Closes the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-closemodule">CloseModule</a>
</td>
<td align="left" width="63%">
Closes the current module

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects the components in a module to the specified feature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-extractcab">ExtractCAB</a>
</td>
<td align="left" width="63%">
Extracts the embedded CAB of a Merge Module to a disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/advpub/nf-advpub-extractfilesa">ExtractFiles</a>
</td>
<td align="left" width="63%">
Creates a source image of the Merge Module beneath the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-log">Log</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-merge">Merge</a>
</td>
<td align="left" width="63%">
Merges the current module into the current database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-opendatabase">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens a database to use as the merge target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-openlog">OpenLog</a>
</td>
<td align="left" width="63%">
Opens a log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/Msi/merge-openmodule">OpenModule</a>
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

<a href="/windows/desktop/Msi/merge-dependencies">Dependencies</a>


</td>
<td align="left" width="63%">
Returns a collection of all unsatisfied dependencies in the database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/Msi/merge-errors">Errors</a>


</td>
<td align="left" width="63%">
Returns a collection of all errors from the most recent merge operation.

</td>
</tr>
</table>