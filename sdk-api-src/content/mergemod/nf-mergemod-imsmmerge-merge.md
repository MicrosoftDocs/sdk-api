---
UID: NF:mergemod.IMsmMerge.Merge
title: IMsmMerge::Merge (mergemod.h)
description: The Merge method executes a merge of the current database and current module.
helpviewer_keywords: ["IMsmMerge interface","Merge method","IMsmMerge.Merge","IMsmMerge::Merge","Merge","Merge method","Merge method","IMsmMerge interface","_msi_merge_function","mergemod/IMsmMerge::Merge","setup.imsmmerge_merge"]
old-location: setup\imsmmerge_merge.htm
tech.root: setup
ms.assetid: 3ff1a2a8-accb-43d7-ba38-a89a5d099dc5
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,Merge method, IMsmMerge.Merge, IMsmMerge::Merge, Merge, Merge method, Merge method,IMsmMerge interface, _msi_merge_function, mergemod/IMsmMerge::Merge, setup.imsmmerge_merge
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
 - IMsmMerge::Merge
 - mergemod/IMsmMerge::Merge
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
 - IMsmMerge.Merge
---

# IMsmMerge::Merge


## -description

The 
<b>Merge</b> method executes a merge of the current database and current module. The merge attaches the components in the module to the feature identified by <i>Feature</i>. The root of the module's directory tree is redirected to the location given by <i>RedirectDir</i>. For more information, see the 
<b>Merge</b> method of the <a href="/windows/desktop/Msi/merge-object">Merge</a> object.  
			

<b>IMsmMerge2::Merge</b>    Mergemod.dll version 2.0 or later.
			<div> </div><b>IMsmMerge::Merge</b>      All Mergemod.dll versions.

## -parameters

### -param Feature [in]

The name of a feature in the database. A <b>LPCWSTR</b> can be used in place of a <b>BSTR</b>.

### -param RedirectDir [in]

The key of an entry in the Directory table of the database. A <b>LPCWSTR</b> can be used in place of a <b>BSTR</b>. This parameter can be null or an empty string.

## -returns

The <b>Merge</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The merge failed catastrophically. This indicates an operational error, and is not the normal error return for a failed merge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded, but there were errors and the merge itself may not be valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
</td>
<td width="60%">
The system ran out of memory and could not complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

This function executes a merge of the current database and current module. The root of the module's directory tree is redirected to the location given by <i>RedirectDir</i>. If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail. Errors can be retrieved using the <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-get_errors">get_Errors</a> function. Errors and informational messages are posted to the current log file.

Note that the 
<b>Merge</b> function gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database. For more information, see 
<a href="/windows/desktop/Msi/referencing-features-in-merge-modules">Referencing Features in Merge Modules</a>.

Once the merge is complete, components in the module are attached to the feature identified by <i>Feature</i>. This feature must already exist and is not created.

The module can be attached to additional features using the 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-connect">Connect</a> function. Note that calling the 
<b>Connect</b> function only creates feature-component associations. It does not modify the rows that have already been merged in to the database.

Changes made to the database are not saved to disk unless 
the <a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closedatabase">CloseDatabase</a> function is called with <i>bCommit</i> set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>