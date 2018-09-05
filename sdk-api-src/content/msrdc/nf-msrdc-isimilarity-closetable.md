---
UID: NF:msrdc.ISimilarity.CloseTable
title: ISimilarity::CloseTable
author: windows-sdk-content
description: Closes the tables in a similarity file.
old-location: rdc\isimilarity_closetable.htm
old-project: Rdc
ms.assetid: 5bf16568-ed61-42a3-91b9-79a1aa731bc0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CloseTable, CloseTable method [Remote Differential Compression], CloseTable method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CloseTable method, ISimilarity.CloseTable, ISimilarity::CloseTable, fs.isimilarity_closetable, msrdc/ISimilarity::CloseTable, rdc.isimilarity_closetable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarity.CloseTable
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarity::CloseTable


## -description


Closes the tables in a similarity file.


## -parameters




### -param isValid [in]

<b>FALSE</b> if the similarity traits table and  similarity file ID table should be deleted when they are closed; otherwise, <b>TRUE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>FALSE</b> is specified for the <i>isValid</i> parameter, only the tables are deleted; the similarity file is not deleted. The caller is responsible for deleting the similarity file.

When the <b>CloseTable</b> method returns, the tables are always closed, even if this method returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

