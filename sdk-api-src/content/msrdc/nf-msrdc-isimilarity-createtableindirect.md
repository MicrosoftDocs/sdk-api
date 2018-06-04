---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ISimilarity::CreateTableIndirect


## -description


Creates or opens a similarity traits table and a similarity file ID table using the RDC application's implementations of the <a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a> and <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interfaces.


## -parameters




### -param mapping [in]

An <a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a> interface pointer initialized to write the similarity traits table to the file.


### -param fileIdFile [in]

An <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interface pointer initialized to 
      write the file ID table to the file.


### -param truncate [in]

<b>TRUE</b> if a new similarity traits table and a new similarity file ID table should always be created or truncated. If <b>FALSE</b> is specified and these tables exist and are valid, they may be used; otherwise, if one of the tables is not valid or does not exist, any existing tables are overwritten.


### -param recordSize [in]

The size, in bytes, of each file ID to be stored in the similarity file ID table. All similarity file IDs must be the same size. The valid range is from <b>SimilarityFileIdMinSize</b> to <b>SimilarityFileIdMaxSize</b>. If existing tables are being opened, the value of this parameter must match the file ID size of the existing similarity file ID table. Otherwise, the existing tables are assumed to be not valid and will be overwritten.


### -param isNew [out]

A pointer to  a variable that receives an  <a href="https://msdn.microsoft.com/f46dd0f0-22b0-41fb-a7c2-29d1b4514f7e">RdcCreatedTables</a> enumeration value that describes the state of the tables. If new tables are created, this variable receives <b>RDCTABLE_New</b>. If existing tables are used, this variable receives <b>RDCTABLE_Existing</b>. If this method fails, this variable receives <b>RDCTABLE_InvalidOrUnknown</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If one of the tables can be created or opened successfully, but the other one cannot, both tables are marked as not valid, and the variable that the <i>isNew</i> parameter points to receives <b>RDCTABLE_InvalidOrUnknown</b>.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>
 

 

