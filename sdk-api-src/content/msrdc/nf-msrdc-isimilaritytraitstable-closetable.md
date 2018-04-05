---
UID: NF:msrdc.ISimilarityTraitsTable.CloseTable
title: ISimilarityTraitsTable::CloseTable method
author: windows-driver-content
description: Closes a similarity traits table.
old-location: rdc\isimilaritytraitstable_closetable.htm
old-project: Rdc
ms.assetid: 941f1e81-035d-4935-bcdf-8c9c6ad9ed4d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CloseTable method [Remote Differential Compression], CloseTable method [Remote Differential Compression], ISimilarityTraitsTable interface, CloseTable,ISimilarityTraitsTable.CloseTable, ISimilarityTraitsTable, ISimilarityTraitsTable interface [Remote Differential Compression], CloseTable method, ISimilarityTraitsTable::CloseTable, fs.isimilaritytraitstable_closetable, msrdc/ISimilarityTraitsTable::CloseTable, rdc.isimilaritytraitstable_closetable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityTraitsTable.CloseTable
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISimilarityTraitsTable::CloseTable method


## -description


Closes a similarity traits table.


## -parameters




### -param isValid [in]

<b>FALSE</b> if the similarity traits table should be deleted when it is closed; otherwise, <b>TRUE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>FALSE</b> is specified for the <i>isValid</i> parameter, only the table is deleted; the similarity file is not deleted. The caller is responsible for deleting the similarity file.

When the <b>CloseTable</b> method returns, the table is always closed, even if this method returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/0985e27c-aa70-43c1-bcec-00ef14f2df58">ISimilarityTraitsTable</a>
 

 

