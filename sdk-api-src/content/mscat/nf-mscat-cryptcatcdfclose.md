---
UID: NF:mscat.CryptCATCDFClose
title: CryptCATCDFClose function
author: windows-sdk-content
description: Closes a catalog definition file (CDF) and frees the memory for the corresponding CRYPTCATCDF structure.
old-location: security\cryptcatcdfclose.htm
tech.root: SecCrypto
ms.assetid: 9f2a1175-f9fe-4f4d-bf6f-e4f4c59739ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptCATCDFClose, CryptCATCDFClose function [Security], mscat/CryptCATCDFClose, security.cryptcatcdfclose
ms.topic: function
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATCDFClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

