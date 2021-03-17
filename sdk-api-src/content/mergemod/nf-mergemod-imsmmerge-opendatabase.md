---
UID: NF:mergemod.IMsmMerge.OpenDatabase
title: IMsmMerge::OpenDatabase (mergemod.h)
description: The OpenDatabase method opens a Windows Installer installation database, located at a specified path, that is to be merged with a module. For more information, see the OpenDatabase method of the Merge object.
helpviewer_keywords: ["IMsmMerge interface","OpenDatabase method","IMsmMerge.OpenDatabase","IMsmMerge::OpenDatabase","OpenDatabase","OpenDatabase method","OpenDatabase method","IMsmMerge interface","_msi_opendatabase_function","mergemod/IMsmMerge::OpenDatabase","setup.imsmmerge_opendatabase"]
old-location: setup\imsmmerge_opendatabase.htm
tech.root: setup
ms.assetid: cafe02a0-2e86-43f6-9cde-e3dd23bdfc4c
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,OpenDatabase method, IMsmMerge.OpenDatabase, IMsmMerge::OpenDatabase, OpenDatabase, OpenDatabase method, OpenDatabase method,IMsmMerge interface, _msi_opendatabase_function, mergemod/IMsmMerge::OpenDatabase, setup.imsmmerge_opendatabase
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
 - IMsmMerge::OpenDatabase
 - mergemod/IMsmMerge::OpenDatabase
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
 - IMsmMerge.OpenDatabase
---

# IMsmMerge::OpenDatabase


## -description

The 
<b>OpenDatabase</b> method opens a Windows Installer installation database, located at a specified path, that is to be merged with a module. For more information, see the 
<a href="/windows/desktop/Msi/merge-opendatabase">OpenDatabase</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. 

<b>IMsmMerge2::OpenDatabase</b>    Mergemod.dll version 2.0 and later.<div> </div><b>IMsmMerge::OpenDatabase</b>      All Mergemod.dll versions.

## -parameters

### -param Path

Path to the database being opened.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There was an error opening the database.

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

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>