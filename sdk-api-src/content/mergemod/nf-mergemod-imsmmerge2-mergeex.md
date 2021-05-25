---
UID: NF:mergemod.IMsmMerge2.MergeEx
title: IMsmMerge2::MergeEx (mergemod.h)
description: The MergeEx method executes a merge of the current database and current module.
helpviewer_keywords: ["IMsmMerge2 interface","MergeEx method","IMsmMerge2.MergeEx","IMsmMerge2::MergeEx","MergeEx","MergeEx method","MergeEx method","IMsmMerge2 interface","_msi_mergeex_function","mergemod/IMsmMerge2::MergeEx","setup.imsmmerge2_mergeex"]
old-location: setup\imsmmerge2_mergeex.htm
tech.root: setup
ms.assetid: fdfd950f-cba9-4b87-ae07-c3d3b127f69d
ms.date: 12/05/2018
ms.keywords: IMsmMerge2 interface,MergeEx method, IMsmMerge2.MergeEx, IMsmMerge2::MergeEx, MergeEx, MergeEx method, MergeEx method,IMsmMerge2 interface, _msi_mergeex_function, mergemod/IMsmMerge2::MergeEx, setup.imsmmerge2_mergeex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge2::MergeEx
 - mergemod/IMsmMerge2::MergeEx
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
 - IMsmMerge2.MergeEx
---

# IMsmMerge2::MergeEx


## -description

The 
<b>MergeEx</b> method executes a merge of the current database and current module. The merge attaches the components in the module to the feature identified by <i>Feature</i>. The root of the module's directory tree is redirected to the location given by <i>RedirectDir</i>. For more information, see the 
<a href="/windows/desktop/Msi/merge-mergeex">MergeEx</a> method of the <a href="/windows/desktop/Msi/merge-object">Merge</a> object.

## -parameters

### -param Feature [in]

The name of a feature in the database. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

### -param RedirectDir [in]

The key of an entry in the Directory table of the database. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>. This parameter may be <b>NULL</b> or an empty string.

### -param pConfiguration [in]

The <i>pConfiguration</i> argument is an interface implemented by the client. The argument may be <b>NULL</b>. The presence of this argument indicates that the client tool is capable of modifying configurable merge modules. The presence of this argument does not require the client to provide configuration data for any specific configurable item.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The merge was stopped due to an error. Some tables may not have been merged. See the Remarks section for more information.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

This function executes a merge of the current database and current module. The root of the module's directory tree is redirected to the location given by <i>RedirectDir</i>. If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail. Errors may be retrieved using 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-get_errors">get_Errors</a> function. Errors and informational messages will be posted to the current log file.

Once the merge is complete, components in the module are attached to the feature identified by <i>Feature</i>. This feature must already exist and is not created. The module may be attached to additional features using 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-connect">Connect</a> function.

Changes made to the database will not be saved to disk unless 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closedatabase">CloseDatabase</a> function is called with <i>bCommit</i> set to <b>TRUE</b>.

When the merge fails because of an incorrect module configuration the function returns E_FAIL. This includes these msmErrorType errors: msmErrorBadNullSubstitution, msmErrorBadSubstitutionType, msmErrorBadNullResponse, msmErrorMissingConfigItem, and msmErrorDataRequestFailed. These errors cause the merge to stop immediately when the error is encountered. The error object is still added to the enumerator when 
<b>MergeEx</b> returns E_FAIL. For more information about msmErrorType errors, see 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmerror-get_type">get_Type Function (Error Object)</a>. All other errors cause 
<b>MergeEx</b> to return S_FALSE and cause the merge to continue.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>