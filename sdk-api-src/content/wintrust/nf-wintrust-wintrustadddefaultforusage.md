---
UID: NF:wintrust.WintrustAddDefaultForUsage
title: WintrustAddDefaultForUsage function
author: windows-sdk-content
description: Specifies the default usage identifier and callback information for a provider.
old-location: security\wintrustadddefaultforusage.htm
tech.root: seccrypto
ms.assetid: 511D05BD-0F8C-45B8-A1B0-D3C7AAFECCFC
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: WintrustAddDefaultForUsage, WintrustAddDefaultForUsage function [Security], security.wintrustadddefaultforusage, wintrust/WintrustAddDefaultForUsage
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
 - WintrustAddDefaultForUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WintrustAddDefaultForUsage function


## -description


The <b>WintrustAddDefaultForUsage</b> function specifies the default usage identifier and callback information for a provider.


## -parameters




### -param pszUsageOID [in]

Pointer to a string that contains the identifier.


### -param psDefUsage [in]

Pointer to a <a href="https://msdn.microsoft.com/A6047CBA-E4BA-4A31-B700-C368CFB57895">CRYPT_PROVIDER_REGDEFUSAGE</a> structure that contains callback information.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b>  if the function fails.   If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function  to determine the reason for failure.




## -remarks



If the provider uses this function and requires any of the callback data, the provider must completely fill out the <a href="https://msdn.microsoft.com/A6047CBA-E4BA-4A31-B700-C368CFB57895">CRYPT_PROVIDER_REGDEFUSAGE</a> structure.

The usage and callback information can be retrieved by calling the <a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a> function.




## -see-also




<a href="https://msdn.microsoft.com/28A93F39-0CBC-432C-841B-83B54A50EA14">CRYPT_PROVIDER_DEFUSAGE</a>



<a href="https://msdn.microsoft.com/A6047CBA-E4BA-4A31-B700-C368CFB57895">CRYPT_PROVIDER_REGDEFUSAGE</a>



<a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a>
 

 

