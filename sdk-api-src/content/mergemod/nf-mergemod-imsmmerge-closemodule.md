---
UID: NF:mergemod.IMsmMerge.CloseModule
title: IMsmMerge::CloseModule (mergemod.h)
description: The CloseModule method closes the currently open Windows Installer merge module. For more information, see the CloseModule method of the Merge object.
helpviewer_keywords: ["CloseModule","CloseModule method","CloseModule method","IMsmMerge interface","IMsmMerge interface","CloseModule method","IMsmMerge.CloseModule","IMsmMerge::CloseModule","_msi_closemodule_function","mergemod/IMsmMerge::CloseModule","setup.imsmmerge_closemodule"]
old-location: setup\imsmmerge_closemodule.htm
tech.root: setup
ms.assetid: bbe8ab14-3d8e-441c-a9bf-0319a9b3a5de
ms.date: 12/05/2018
ms.keywords: CloseModule, CloseModule method, CloseModule method,IMsmMerge interface, IMsmMerge interface,CloseModule method, IMsmMerge.CloseModule, IMsmMerge::CloseModule, _msi_closemodule_function, mergemod/IMsmMerge::CloseModule, setup.imsmmerge_closemodule
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
 - IMsmMerge::CloseModule
 - mergemod/IMsmMerge::CloseModule
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
 - IMsmMerge.CloseModule
---

# IMsmMerge::CloseModule


## -description

The 
<b>CloseModule</b> method closes the currently open Windows Installer merge module. For more information, see the 
<a href="/windows/desktop/Msi/merge-closemodule">CloseModule</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge object</a>. 

<b>IMsmMerge2::CloseDatabase</b>    Mergemod.dll version 2.0 or later.<div> </div>
<a href="/windows/desktop/api/mergemod/nf-mergemod-imsmmerge-closedatabase">IMsmMerge::CloseDatabase</a>      All Mergemod.dll versions.



## -returns

The <b>CloseModule</b> function returns the following values.

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
There was an error closing the module. The state of the 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge">IMsmMerge</a> or 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge2">IMsmMerge2</a> interface is now undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No module was open.

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

Closing a merge module does not affect any errors that have not been retrieved.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
