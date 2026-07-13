---
UID: NF:msrdc.ISimilarity.CloseTable
title: ISimilarity::CloseTable (msrdc.h)
description: Closes the tables in a similarity file.
helpviewer_keywords: ["CloseTable","CloseTable method [Remote Differential Compression]","CloseTable method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","CloseTable method","ISimilarity.CloseTable","ISimilarity::CloseTable","fs.isimilarity_closetable","msrdc/ISimilarity::CloseTable","rdc.isimilarity_closetable"]
old-location: rdc\isimilarity_closetable.htm
tech.root: rdc
ms.assetid: 5bf16568-ed61-42a3-91b9-79a1aa731bc0
ms.date: 12/05/2018
ms.keywords: CloseTable, CloseTable method [Remote Differential Compression], CloseTable method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CloseTable method, ISimilarity.CloseTable, ISimilarity::CloseTable, fs.isimilarity_closetable, msrdc/ISimilarity::CloseTable, rdc.isimilarity_closetable
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
 - ISimilarity::CloseTable
 - msrdc/ISimilarity::CloseTable
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
 - ISimilarity.CloseTable
---

# ISimilarity::CloseTable


## -description

Closes the tables in a similarity file.

## -parameters

### -param isValid [in]

<b>FALSE</b> if the similarity traits table and  similarity file ID table should be deleted when they are closed; otherwise, <b>TRUE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <b>FALSE</b> is specified for the <i>isValid</i> parameter, only the tables are deleted; the similarity file is not deleted. The caller is responsible for deleting the similarity file.

When the <b>CloseTable</b> method returns, the tables are always closed, even if this method returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>