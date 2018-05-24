---
UID: NF:msdrm.DRMGetRightInfo
title: DRMGetRightInfo function
author: windows-driver-content
description: Obtains information about a previously created right.
old-location: rm\drmgetrightinfo.htm
old-project: AdRms_Sdk
ms.assetid: 54581da2-d3d1-44ee-936a-568b7d66143b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMGetRightInfo, DRMGetRightInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetRightInfo, rm.drmgetrightinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMGetRightInfo
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetRightInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetRightInfo</b> function obtains information about a previously created right.


## -parameters




### -param hRight [in]

The handle of the right to retrieve information from.


### -param puRightNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszRightName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszRightName</i> buffer.


### -param wszRightName [out]

A pointer to a null-terminated Unicode string that receives the name of the right. The size of this buffer is specified by the <i>puRightNameLength</i> parameter. If this information is not required, set this parameter to <b>NULL</b>.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puRightNameLength</i> value.


### -param pstFrom [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the starting validity time, in UTC time, of the right. If this information is not required, set this parameter to <b>NULL</b>.


### -param pstUntil [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the ending validity time, in UTC time, of the right. If this information is not required, set this parameter to <b>NULL</b>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>



<a href="https://msdn.microsoft.com/05074fbd-9268-41b4-a916-a932dc7a7858">DRMCreateRight</a>
 

 

