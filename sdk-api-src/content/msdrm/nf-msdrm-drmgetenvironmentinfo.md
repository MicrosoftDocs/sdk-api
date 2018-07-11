---
UID: NF:msdrm.DRMGetEnvironmentInfo
title: DRMGetEnvironmentInfo function
author: windows-sdk-content
description: Returns information about a secure environment.
old-location: rm\drmgetenvironmentinfo.htm
old-project: adrms_sdk
ms.assetid: 6b6dd54f-1835-42da-b151-9da9139efeb3
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DRMGetEnvironmentInfo, DRMGetEnvironmentInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetEnvironmentInfo, rm.drmgetenvironmentinfo
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
 - DRMGetEnvironmentInfo
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DRMGetEnvironmentInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]
<p class="CCE_Message">[The <b>DRMGetEnvironmentInfo</b> function is no longer supported and returns S_OK. Instead, use the <a href="https://msdn.microsoft.com/6cb1275a-c0e4-48df-a389-76add74bdabd">DRMGetInfo</a> function.]

The <b>DRMGetEnvironmentInfo</b> function returns information about a secure environment.


## -parameters




### -param handle [in]

Environment handle.


### -param wszAttribute [in]

The attribute to query for. In Rights Management Services client 1.0 SP1, the only supported attribute is <b>g_wszQUERY_BLOCKSIZE</b>. In Rights Management Services client 1.0, the attributes that can be queried are listed in the header file Msdrmgetinfo.h. Attributes include <b>g_wszQUERY_MANIFESTSOURCE</b> and <b>g_wszQUERY_APIVERSION</b>.


### -param peEncoding [out]

Encoding type used.


### -param pcBuffer [in, out]

A pointer to a UINT value that, on input, contains the size of the buffer pointed to by the <i>pbBuffer</i> parameter. The size of the buffer is expressed as the number of Unicode characters, including the terminating null character. On output, the value contains the number of characters copied to the buffer. The number copied includes the terminating null character.


### -param pbBuffer [out]

A pointer to a null-terminated Unicode string that receives the value associated with the attribute specified by the <i>wszAttribute</i> parameter. The size of this buffer is specified by the <i>pcBuffer</i> parameter. The size is expressed as the number of Unicode characters, including the terminating null character.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function returns information only about environment handles. For information about other handles, see <a href="https://msdn.microsoft.com/6cb1275a-c0e4-48df-a389-76add74bdabd">DRMGetInfo</a>.

Memory allocation and deallocation are handled by the caller.To create a buffer and retrieve environment information, perform the following steps:

<ol>
<li>Call <b>DRMGetEnvironmentInfo</b> with <i>pbBuffer</i> equal to <b>NULL</b>. The function returns the required number of Unicode characters, including the terminating NULL character, in the <i>pcBuffer</i> parameter.</li>
<li>Allocate memory for the buffer. Remember that a Unicode character is two bytes long.</li>
<li>Call <b>DRMGetEnvironmentInfo</b> again with 
<i>pbBuffer</i> equal to the pointer you created when allocating the buffer.</li>
<li>When you have finished using the memory, free it.</li>
</ol>


In Rights Management Services client 1.0 SP1, the only supported attribute is <b>g_wszQUERY_BLOCKSIZE</b>. For the attributes that can be queried in Rights Management Services client 1.0, see the Msdrmgetinfo.h header file that installs with this SDK.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/6cb1275a-c0e4-48df-a389-76add74bdabd">DRMGetInfo</a>
 

 

