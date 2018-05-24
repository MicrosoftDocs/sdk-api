---
UID: NF:msrdc.ISimilarity.CopyAndSwap
title: ISimilarity::CopyAndSwap
author: windows-driver-content
description: Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.
old-location: rdc\isimilarity_copyandswap.htm
old-project: Rdc
ms.assetid: 3a31530e-da6d-4ac8-9fd4-d91419777ce5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CopyAndSwap, CopyAndSwap method [Remote Differential Compression], CopyAndSwap method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],CopyAndSwap method, ISimilarity.CopyAndSwap, ISimilarity::CopyAndSwap, fs.isimilarity_copyandswap, msrdc/ISimilarity::CopyAndSwap, rdc.isimilarity_copyandswap
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
-	ISimilarity.CopyAndSwap
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarity::CopyAndSwap


## -description


 Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.

After the <b>CopyAndSwap</b> method returns, the application continues to use the same <a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a> object that it used before calling this method. However, the <b>ISimilarity</b> object is now associated with a different similarity file on disk.


## -parameters




### -param newSimilarityTables [in, optional]

An optional pointer to a temporary <a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a> object that is used to create temporary copies of the tables. Before calling the <b>CopyAndSwap</b> method, the caller must call the <a href="https://msdn.microsoft.com/808c20f9-054d-475d-8ca3-ee2dde871426">CreateTable</a> method to create the temporary tables. On return, the caller must call the <a href="https://msdn.microsoft.com/5bf16568-ed61-42a3-91b9-79a1aa731bc0">CloseTable</a> method to close the temporary tables.


### -param reportProgress [in, optional]

An optional pointer to an <a href="https://msdn.microsoft.com/813bda93-08d5-456c-9bde-ce6dd53fb8bf">ISimilarityReportProgress</a> object that will receive information on the progress of the copy-and-swap operation and allow the application to stop the copy operation. The caller must release this interface when it is no longer needed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a>



<a href="https://msdn.microsoft.com/e393290b-02d3-4265-9252-f5541e4054ce">ISimilarityReportProgress::ReportProgress</a>
 

 

