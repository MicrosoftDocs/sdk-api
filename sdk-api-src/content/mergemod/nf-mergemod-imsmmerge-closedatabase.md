---
UID: NF:mergemod.IMsmMerge.CloseDatabase
title: IMsmMerge::CloseDatabase (mergemod.h)
description: The CloseDatabase method closes the currently open Windows Installer database. For more information, see the CloseDatabase method of the Merge object.
helpviewer_keywords: ["CloseDatabase","CloseDatabase method","CloseDatabase method","IMsmMerge interface","IMsmMerge interface","CloseDatabase method","IMsmMerge.CloseDatabase","IMsmMerge::CloseDatabase","_msi_closedatabase_function","mergemod/IMsmMerge::CloseDatabase","setup.imsmmerge_closedatabase"]
old-location: setup\imsmmerge_closedatabase.htm
tech.root: setup
ms.assetid: efbb6238-e9e3-4603-896a-75fcff2bb362
ms.date: 12/05/2018
ms.keywords: CloseDatabase, CloseDatabase method, CloseDatabase method,IMsmMerge interface, IMsmMerge interface,CloseDatabase method, IMsmMerge.CloseDatabase, IMsmMerge::CloseDatabase, _msi_closedatabase_function, mergemod/IMsmMerge::CloseDatabase, setup.imsmmerge_closedatabase
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
 - IMsmMerge::CloseDatabase
 - mergemod/IMsmMerge::CloseDatabase
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
 - IMsmMerge.CloseDatabase
---

# IMsmMerge::CloseDatabase


## -description

The 
<b>CloseDatabase</b> method closes the currently open Windows Installer database. For more information, see the 
<a href="/windows/desktop/Msi/merge-closedatabase">CloseDatabase</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge object</a>. 

<b>IMsmMerge2::CloseDatabase</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::CloseDatabase</b>      All Mergemod.dll versions.

## -parameters

### -param Commit

<b>TRUE</b> if changes should be saved, <b>FALSE</b> otherwise.

## -returns

The <b>CloseDatabase</b> function returns the following values.

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
There was an error closing the database. The state of the 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge">IMsmMerge</a> or 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge2">IMsmMerge2</a> interface is now in an undefined state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No database was open.

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
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_CANTSAVE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Unable to save database. This error is not generated if <i>bCommit</i> is <b>FALSE</b>.

</td>
</tr>
</table>

## -remarks

This function closes the currently open database. Closing a database clears all dependency information but does not affect any errors that have not been retrieved.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>