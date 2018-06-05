---
UID: NF:msrdc.ISimilarityTraitsMapping.CloseMapping
title: ISimilarityTraitsMapping::CloseMapping
author: windows-sdk-content
description: Closes a file mapping object for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping_closemapping.htm
old-project: Rdc
ms.assetid: 9ac20c6b-9fe5-4b59-a9ed-faef97fd76f2
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CloseMapping, CloseMapping method [Remote Differential Compression], CloseMapping method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],CloseMapping method, ISimilarityTraitsMapping.CloseMapping, ISimilarityTraitsMapping::CloseMapping, fs.isimilaritytraitsmapping_closemapping, msrdc/ISimilarityTraitsMapping::CloseMapping, rdc.isimilaritytraitsmapping_closemapping
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
-	ISimilarityTraitsMapping.CloseMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMapping::CloseMapping


## -description


Closes a file mapping object for a similarity traits table file.


## -parameters






## -returns



This method does not return a value.




## -remarks



Note that there may still be valid views open on the file. No new views may be created after the mapping is closed, but existing views continue to work.




## -see-also




<a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a>
 

 

