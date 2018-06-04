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

# CryptCATCDFClose function


## -description


<p class="CCE_Message">[The  <b>CryptCATCDFClose</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCDFClose</b> function closes a catalog definition file (CDF) and frees the memory for the corresponding <a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a> structure. <b>CryptCATCDFClose</b> is called by <a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>.


## -parameters




### -param pCDF [in]

A pointer to a <a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a> structure.


## -returns



Upon success, this function returns <b>TRUE</b>. The <b>CryptCATCDFClose</b> function returns <b>FALSE</b> with an <b>ERROR_INVALID_PARAMETER</b> error if it fails.




## -remarks



Before closing the catalog output file specified in  <i>pCDF</i>, the <b>CryptCATCDFClose</b> function signs and persists it to the file system.




## -see-also




<a href="https://msdn.microsoft.com/15d5710a-d4df-4e45-b161-5d4f7509ba29">CRYPTCATCDF</a>



<a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>
 

 

