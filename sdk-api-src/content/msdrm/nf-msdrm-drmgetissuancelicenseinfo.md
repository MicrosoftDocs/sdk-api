---
UID: NF:msdrm.DRMGetIssuanceLicenseInfo
title: DRMGetIssuanceLicenseInfo function
author: windows-sdk-content
description: Retrieves various information from an issuance license.
old-location: rm\drmgetissuancelicenseinfo.htm
tech.root: AdRms_Sdk
ms.assetid: 67213b97-3831-4284-b807-f6bc69d4b610
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRMGetIssuanceLicenseInfo, DRMGetIssuanceLicenseInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetIssuanceLicenseInfo, rm.drmgetissuancelicenseinfo
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMGetIssuanceLicenseInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetIssuanceLicenseInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetIssuanceLicenseInfo</b> function retrieves various information from an issuance license.


## -parameters




### -param hIssuanceLicense [in]

A handle to the issuance license to retrieve information from.


### -param pstTimeFrom [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the starting validity time, in UTC time, of the license. If this information is not required, set this parameter to <b>NULL</b>.


### -param pstTimeUntil [out]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that receives the ending validity time, in UTC time, of the license. If this information is not required, set this parameter to <b>NULL</b>.


### -param uFlags [in]

A value of the <a href="https://msdn.microsoft.com/09e586bc-bf0e-4831-be35-f00a6288231e">DRM_DISTRIBUTION_POINT_INFO</a> enumeration that specifies the type of service provided by this distribution point (such as publishing or license acquisition). Only one flag can be used.


### -param puDistributionPointNameLength [in, out]

A pointer to a UINT value that, on entry, contains the length, in characters, of the <i>wszDistributionPointName</i> buffer. This size must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszDistributionPointName</i> buffer.

If the <i>wszDistributionPointName</i> string is not required, set this parameter to <b>NULL</b>.


### -param wszDistributionPointName [out]

A pointer to a null-terminated Unicode string that receives the name of a website that can distribute end-user licenses. The size of this buffer is specified by the <i>puDistributionPointNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puDistributionPointNameLength</i> value.


### -param puDistributionPointURLLength [in, out]

A pointer to a UINT value that, on entry, contains the length, in characters, of the <i>wszDistributionPointURL</i> buffer. This size must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszDistributionPointURL</i> buffer.

If the <i>wszDistributionPointURL</i> string is not required, set this parameter to <b>NULL</b>.


### -param wszDistributionPointURL [out]

A pointer to a null-terminated Unicode string that receives the URL of a website that can distribute end-user licenses. The size of this buffer is specified by the <i>puDistributionPointURLLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puDistributionPointURLLength</i> value.


### -param phOwner [out]

A pointer to a <b>DRMPUBHANDLE</b> value that receives the handle of the issuance license owner. If this information is not required, set this parameter to <b>NULL</b>. Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle.


### -param pfOfficial [out]

A pointer to  a Boolean value that specifies whether the issuance license is based on an official template. A nonzero value indicates that the license is based on an official template. Official templates are created and signed by the AD RMS server. Unofficial templates are created by the client from scratch or by adapting an official template. If this information is not required, set this parameter to <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/6b99d3d2-3144-450d-8e9d-18c881718ace">Creating a License From a Template</a>.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Memory allocation and release for out parameters are the responsibility of the calling function. To determine the buffer size needed to hold these values, first call this function with <b>NULL</b> in <i>wszDistributionPointName</i> and <i>wszDistributionPointURL</i> to retrieve the required sizes from the length parameters <i>puDistributionPointNameLength</i> and <i>puDistributionPointURLLength</i>.

Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the license owner handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a>
 

 

