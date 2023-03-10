---
UID: NF:msrdc.ISimilarityFileIdTable.CloseTable
title: ISimilarityFileIdTable::CloseTable (msrdc.h)
description: Closes a similarity file ID table.
helpviewer_keywords: ["CloseTable","CloseTable method [Remote Differential Compression]","CloseTable method [Remote Differential Compression]","ISimilarityFileIdTable interface","ISimilarityFileIdTable interface [Remote Differential Compression]","CloseTable method","ISimilarityFileIdTable.CloseTable","ISimilarityFileIdTable::CloseTable","fs.isimilarityfileidtable_closetable","msrdc/ISimilarityFileIdTable::CloseTable","rdc.isimilarityfileidtable_closetable"]
old-location: rdc\isimilarityfileidtable_closetable.htm
tech.root: rdc
ms.assetid: f7c54c1a-0b02-43ae-975c-e94bd3dcac45
ms.date: 12/05/2018
ms.keywords: CloseTable, CloseTable method [Remote Differential Compression], CloseTable method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],CloseTable method, ISimilarityFileIdTable.CloseTable, ISimilarityFileIdTable::CloseTable, fs.isimilarityfileidtable_closetable, msrdc/ISimilarityFileIdTable::CloseTable, rdc.isimilarityfileidtable_closetable
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityFileIdTable::CloseTable
 - msrdc/ISimilarityFileIdTable::CloseTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityFileIdTable.CloseTable
---

# ISimilarityFileIdTable::CloseTable


## -description

Closes a similarity file ID table.

## -parameters

### -param isValid

<b>FALSE</b> if the similarity file ID table should be deleted when it is closed; otherwise, <b>TRUE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <b>FALSE</b> is specified for the <i>isValid</i> parameter, only the table is deleted; the similarity file is not deleted. The caller is responsible for deleting the similarity file.

When the <b>CloseTable</b> method returns, the table is always closed, even if this method returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarityfileidtable">ISimilarityFileIdTable</a>