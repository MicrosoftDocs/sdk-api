---
UID: NF:wintrust.WTHelperProvDataFromStateData
title: WTHelperProvDataFromStateData function
author: windows-sdk-content
description: Retrieves trust provider information from a specified handle.
old-location: security\wthelperprovdatafromstatedata.htm
tech.root: seccrypto
ms.assetid: ca2ca612-2da6-4fe1-8b1e-bc6307eb92af
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: WTHelperProvDataFromStateData, WTHelperProvDataFromStateData function [Security], security.wthelperprovdatafromstatedata, wintrust/WTHelperProvDataFromStateData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wintrust.h
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
req.lib: Wintrust.lib
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
 - WTHelperProvDataFromStateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTHelperProvDataFromStateData function


## -description


<p class="CCE_Message">[The <b>WTHelperProvDataFromStateData</b> function is available for use in  the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperProvDataFromStateData</b> function retrieves trust provider information from a specified handle. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hStateData [in]

A handle previously set by the <a href="https://msdn.microsoft.com/209c9953-a4a5-4ff0-961f-92e97ccce23d">WinVerifyTrustEx</a> function as the <b>hWVTStateData</b>	 member of the <a href="https://msdn.microsoft.com/8fb68f44-6f69-4eac-90de-02689e3e86cf">WINTRUST_DATA</a> structure.


## -returns



If the function succeeds, the function returns a pointer to a <a href="https://msdn.microsoft.com/93ea2ad5-65da-4daa-bfd4-e3d1307829b2">CRYPT_PROVIDER_DATA</a> structure. The returned pointer can be used by the <a href="https://msdn.microsoft.com/8e1ebf82-73c2-445b-9964-6739f7c90c47">WTHelperGetProvSignerFromChain</a>   function.

If the function fails, it returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/8e1ebf82-73c2-445b-9964-6739f7c90c47">WTHelperGetProvSignerFromChain</a>
 

 

