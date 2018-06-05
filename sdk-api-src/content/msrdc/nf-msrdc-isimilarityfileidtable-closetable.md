---
UID: NF:msrdc.ISimilarityFileIdTable.CloseTable
title: ISimilarityFileIdTable::CloseTable
author: windows-sdk-content
description: Closes a similarity file ID table.
old-location: rdc\isimilarityfileidtable_closetable.htm
old-project: Rdc
ms.assetid: f7c54c1a-0b02-43ae-975c-e94bd3dcac45
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CloseTable, CloseTable method [Remote Differential Compression], CloseTable method [Remote Differential Compression],ISimilarityFileIdTable interface, ISimilarityFileIdTable interface [Remote Differential Compression],CloseTable method, ISimilarityFileIdTable.CloseTable, ISimilarityFileIdTable::CloseTable, fs.isimilarityfileidtable_closetable, msrdc/ISimilarityFileIdTable::CloseTable, rdc.isimilarityfileidtable_closetable
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityFileIdTable.CloseTable
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityFileIdTable::CloseTable


## -description


Closes a similarity file ID table.


## -parameters




### -param isValid

<b>FALSE</b> if the similarity file ID table should be deleted when it is closed; otherwise, <b>TRUE</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>FALSE</b> is specified for the <i>isValid</i> parameter, only the table is deleted; the similarity file is not deleted. The caller is responsible for deleting the similarity file.

When the <b>CloseTable</b> method returns, the table is always closed, even if this method returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/539a2e9b-9719-4012-bb7f-4d14723a3695">ISimilarityFileIdTable</a>
 

 

