---
UID: NF:msrdc.ISimilarityFileIdTable.Lookup
title: ISimilarityFileIdTable::Lookup
author: windows-sdk-content
description: Retrieves the file ID that corresponds to a given file index in the similarity file ID table.
old-location: rdc\isimilarityfileidtable_lookup.htm
old-project: Rdc
ms.assetid: bf9dbeb1-0182-4927-80ad-bb51fab2e637
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISimilarityFileIdTable interface [Remote Differential Compression],Lookup method, ISimilarityFileIdTable.Lookup, ISimilarityFileIdTable::Lookup, Lookup, Lookup method [Remote Differential Compression], Lookup method [Remote Differential Compression],ISimilarityFileIdTable interface, fs.isimilarityfileidtable_lookup, msrdc/ISimilarityFileIdTable::Lookup, rdc.isimilarityfileidtable_lookup
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
 - ISimilarityFileIdTable.Lookup
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityFileIdTable::Lookup


## -description


Retrieves the file ID that corresponds to a given file index in the similarity file ID table.


## -parameters




### -param similarityFileIndex [in]

The file index that was previously returned for the file ID by the <a href="https://msdn.microsoft.com/2157d6e6-0d60-45a2-9f5c-4096088cb2bb">ISimilarityFileIdTable::Append</a> method.


### -param similarityFileId [out]

A pointer to a variable that receives the file ID. If the file has been marked as not valid, the file ID receives zero.


## -returns



Returns <b>S_OK</b> on success, or an error <b>HRESULT</b> on failure.

This method can also return the following error code.




## -see-also




<a href="https://msdn.microsoft.com/539a2e9b-9719-4012-bb7f-4d14723a3695">ISimilarityFileIdTable</a>
 

 

