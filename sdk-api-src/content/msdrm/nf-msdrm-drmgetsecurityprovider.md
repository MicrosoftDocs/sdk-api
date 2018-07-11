---
UID: NF:msdrm.DRMGetSecurityProvider
title: DRMGetSecurityProvider function
author: windows-sdk-content
description: Retrieves the path to a lockbox.
old-location: rm\drmgetsecurityprovider.htm
old-project: adrms_sdk
ms.assetid: 9f74fd19-bd87-4e21-a2b9-66b7d1f481a1
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DRMGetSecurityProvider, DRMGetSecurityProvider function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetSecurityProvider, rm.drmgetsecurityprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetSecurityProvider
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetSecurityProvider function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetSecurityProvider</b> function retrieves the path to a lockbox.


## -parameters




### -param uFlags [in]

Reserved.


### -param puTypeLen [in, out]

On input, length of the allocated <i>wszType</i> buffer. On output, actual length, in characters, plus one for a null terminator, of the value returned by <i>wszType</i>.


### -param wszType [out]

Type of security provider (such as "filename").


### -param puPathLen [in, out]

On input, length of the allocated <i>wszPath</i> buffer. On output, actual length, in characters, plus one for a null terminator, of the value returned by <i>wszPath</i>.


### -param wszPath [out]

Path to the lockbox.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



When you obtain the output values, first call this function with both <i>wszType</i> and <i>wszPath</i> set to <b>NULL</b> to obtain the needed buffer sizes through <i>puTypeLen</i> and <i>puPathLen</i>. If you set only one buffer pointer to <b>NULL</b>, an error is generated. It is the application's responsibility to allocate and free buffer space.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

