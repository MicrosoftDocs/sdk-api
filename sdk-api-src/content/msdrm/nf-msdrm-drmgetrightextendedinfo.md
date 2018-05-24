---
UID: NF:msdrm.DRMGetRightExtendedInfo
title: DRMGetRightExtendedInfo function
author: windows-driver-content
description: Retrieves custom name-value pairs attached to a right.
old-location: rm\drmgetrightextendedinfo.htm
old-project: AdRms_Sdk
ms.assetid: d228660a-3c20-403e-9a89-e35195b19f92
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DRMGetRightExtendedInfo, DRMGetRightExtendedInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetRightExtendedInfo, rm.drmgetrightextendedinfo
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
-	DRMGetRightExtendedInfo
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMGetRightExtendedInfo function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetRightExtendedInfo</b> function retrieves custom name-value pairs attached to a right.


## -parameters




### -param hRight [in]

The handle of the right to retrieve information from.


### -param uIndex [in]

The zero-based index of the name-value pair to retrieve.


### -param puExtendedInfoNameLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszExtendedInfoName</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszExtendedInfoName</i> buffer.


### -param wszExtendedInfoName [out]

A pointer to a null-terminated Unicode string that receives the name of the item. The size of this buffer is specified by the <i>puExtendedInfoNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puExtendedInfoNameLength</i> value.


### -param puExtendedInfoValueLength [in, out]

A pointer to a <b>UINT</b> value that, on entry, contains the length, in characters, of the <i>wszExtendedInfoValue</i> buffer. This length must include the terminating null character.

After the function returns, this value contains the number of characters, including the terminating null character, that were copied to the <i>wszExtendedInfoValue</i> buffer.


### -param wszExtendedInfoValue [out]

A pointer to a null-terminated Unicode string that receives the value associated with the name. The size of this buffer is specified by the <i>puExtendedInfoValueLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puExtendedInfoValueLength</i> value.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>DRMGetRightExtendedInfo</b> method allows a user to add or retrieve arbitrary strings for a right. Applications can use this string to create generic conditions or add any other information associated with a right. These name-value pairs are added in <a href="https://msdn.microsoft.com/05074fbd-9268-41b4-a916-a932dc7a7858">DRMCreateRight</a> as parallel arrays.

To enumerate the existing extended data values, iterate through the index numbers, starting at zero, until the function returns <b>E_DRM_NO_MORE_DATA</b>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 

