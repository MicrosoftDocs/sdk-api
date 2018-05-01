---
UID: NF:msdrm.DRMCreateRight
title: DRMCreateRight function
author: windows-driver-content
description: Creates an XrML right that will define a right granted to a user or group.
old-location: rm\drmcreateright.htm
old-project: AdRms_Sdk
ms.assetid: 05074fbd-9268-41b4-a916-a932dc7a7858
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: DRMCreateRight, DRMCreateRight function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateRight, rm.drmcreateright
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
-	DRMCreateRight
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateRight function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateRight</b> function creates an XrML right that will define a right granted to a user or group.


## -parameters




### -param wszRightName [in]

A pointer to a null-terminated Unicode string that contains the name of a user-defined or standard XrML (version 1.2) right. For more information, see <a href="https://msdn.microsoft.com/376dcfad-ca65-4540-80a8-7eea3a0e3ad5">Official Template XrML</a>.


### -param pstFrom [in]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the time, in UTC time, when this right will become valid. For more information, see Remarks. Both <i>pstFrom</i> and <i>pstUntil</i> must be specified, or both must be <b>NULL</b>.


### -param pstUntil [in]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the time, in UTC time, when this right will expire. For more information, see Remarks. Both <i>pstFrom</i> and <i>pstUntil</i> must be specified, or both must be <b>NULL</b>.


### -param cExtendedInfo [in]

The number of elements in the <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> arrays. If this parameter is zero, then both the <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> parameters must be <b>NULL</b>.


### -param pwszExtendedInfoName [in]

An array of null-terminated Unicode string pointers that contains the names of extended information data. Each name in this array must be unique. The <b>cExtendedInfo</b> parameter contains the number of elements in this array.


### -param pwszExtendedInfoValue [in]

An array of null-terminated Unicode string pointers that contains the values of the extended information items.  The <b>cExtendedInfo</b> parameter contains the number of elements in this array.


### -param phRight [out]

A pointer to a handle that receives the handle of the created right. This handle can be used with the <a href="https://msdn.microsoft.com/10b76b20-cee7-44f3-b9bd-2b690fdd040c">DRMAddRightWithUser</a> function to bind the right to a user. Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Determining which rights a user can be granted is the responsibility of the application. The only right that Active Directory Rights Management Services enforces is EDIT, which grants the user the right to modify content.

A right can have any name that can be validly expressed in XML.

The <i>pstFrom</i> and <i>pstUntil</i> parameters specify the start and end validity times of the right. These parameters must either both be specified, or both be <b>NULL</b>. An application cannot set only one validity time.

One problem that can arise when creating licenses with short validity times is the problem of clock skew. <i>Clock skew</i> is when the publishing computer's clock and the end user's computer clock are not exactly aligned. Clock skew can cause attempts to exercise rights to fail. For more information, see <a href="https://msdn.microsoft.com/a265b2e8-b8ea-41d3-ae51-ca6019d68221">Clock Skew</a>.

The <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> parameters are pointers to two parallel arrays that associate name-value pairs that hold additional right-specific information. These name-value pairs can specify any additional information you want, and they are retrieved by index number by using <a href="https://msdn.microsoft.com/d228660a-3c20-403e-9a89-e35195b19f92">DRMGetRightExtendedInfo</a>. Extended information items are optional, but if a name or value is given, the corresponding item in the other array cannot be <b>NULL</b>.

Call <a href="https://msdn.microsoft.com/a263a1a8-01b8-4ca6-aefb-f4374459c0c0">DRMClosePubHandle</a> to close the handle of the right created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/9948c2a4-cb42-42c1-bd22-33d39c039391">Creating and Using Issuance Licenses</a>



<a href="https://msdn.microsoft.com/19387d86-6dbc-436f-8772-b9f25458460e">OnlineSigning_GetUnsignedIL.cpp</a>
 

 

