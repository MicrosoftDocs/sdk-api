---
UID: NF:msrdc.ISimilarity.GetRecordCount
title: ISimilarity::GetRecordCount
author: windows-sdk-content
description: Retrieves the number of records that are stored in the similarity file ID table in a similarity file.
old-location: rdc\isimilarity_getrecordcount.htm
tech.root: Rdc
ms.assetid: 19dda0ed-0f11-4e17-823b-667a48cf6dc1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRecordCount, GetRecordCount method [Remote Differential Compression], GetRecordCount method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],GetRecordCount method, ISimilarity.GetRecordCount, ISimilarity::GetRecordCount, fs.isimilarity_getrecordcount, msrdc/ISimilarity::GetRecordCount, rdc.isimilarity_getrecordcount
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarity.GetRecordCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarity::GetRecordCount


## -description


Retrieves the number of records that are stored in the similarity file ID table in a similarity file.


## -parameters




### -param recordCount [out]

A pointer to a variable that receives the number of records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

