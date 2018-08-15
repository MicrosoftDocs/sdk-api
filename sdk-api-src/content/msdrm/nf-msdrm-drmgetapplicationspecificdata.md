---
UID: NF:msdrm.DRMGetApplicationSpecificData
title: DRMGetApplicationSpecificData function
author: windows-sdk-content
description: Retrieves a name-value pair of arbitrary application-specific information.
old-location: rm\drmgetapplicationspecificdata.htm
old-project: adrms_sdk
ms.assetid: 49b23f00-bc73-4f51-8bbe-f523ae2408d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMGetApplicationSpecificData, DRMGetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetApplicationSpecificData, rm.drmgetapplicationspecificdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.redist: 
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
 - DRMGetApplicationSpecificData
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetApplicationSpecificData function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetApplicationSpecificData</b> function retrieves a name-value pair of arbitrary application-specific information.


## -parameters




### -param hIssuanceLicense [in]

A handle to the issuance license to obtain the data from.


### -param uIndex [in]

The zero-based index of the name-value pair in the array of stored name-value pairs to retrieve.


### -param puNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.


### -param wszName [out]

A pointer to a Unicode character buffer that receives the name portion of the name-value pair. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> value.


### -param puValueLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszValue</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszValue</i> buffer.


### -param wszValue [out]

A pointer to a Unicode character buffer that receives the value portion of the name-value pair. The size of this buffer is specified by the <i>puValueLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puValueLength</i> value.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function can be used to retrieve arbitrary information that was stored in the issuance license by using the <a href="https://msdn.microsoft.com/659b2d73-1160-4e5a-8779-4bb272653c54">DRMSetApplicationSpecificData</a> function.

The calling application is responsible for memory allocation/deallocation for variables used to hold retrieved data. To determine the size of the data that will be returned, call this function with <b>NULL</b> in <i>wszValue</i> and <i>wszName</i> to retrieve data sizes from <i>puNameLength</i> and <i>puValueLength</i>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/659b2d73-1160-4e5a-8779-4bb272653c54">DRMSetApplicationSpecificData</a>
 

 

