---
UID: NF:mergemod.IMsmMerge.Connect
title: IMsmMerge::Connect (mergemod.h)
description: The Connect method connects a module that has been, or will be, merged into the database to an additional feature. For more information, see the Connect method of the Merge object.
helpviewer_keywords: ["Connect","Connect method","Connect method","IMsmMerge interface","IMsmMerge interface","Connect method","IMsmMerge.Connect","IMsmMerge::Connect","_msi_connect_function","mergemod/IMsmMerge::Connect","setup.imsmmerge_connect"]
old-location: setup\imsmmerge_connect.htm
tech.root: setup
ms.assetid: f491beb8-90f7-4e41-891d-ef674306339d
ms.date: 12/05/2018
ms.keywords: Connect, Connect method, Connect method,IMsmMerge interface, IMsmMerge interface,Connect method, IMsmMerge.Connect, IMsmMerge::Connect, _msi_connect_function, mergemod/IMsmMerge::Connect, setup.imsmmerge_connect
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
 - IMsmMerge::Connect
 - mergemod/IMsmMerge::Connect
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
 - IMsmMerge.Connect
---

# IMsmMerge::Connect


## -description

The 
<b>Connect</b> method connects a module that has been, or will be, merged into the database to an additional feature. For more information, see the 
<a href="/windows/desktop/Msi/merge-connect">Connect</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. 

<b>IMsmMerge2::Connect</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::Connect</b>      All Mergemod.dll versions.

## -parameters

### -param Feature [in]

The name of a feature in the database. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.

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
The connect failed.

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

The feature must exist before this function is called. Errors may be retrieved using 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-get_errors">get_Errors</a>. Errors and informational messages are posted to the current log file.

Changes made to the database are not be saved to disk unless 
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closedatabase">CloseDatabase</a> function is called with <i>bCommit</i> set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>