---
UID: NF:msdrm.DRMCreateRight
title: DRMCreateRight function (msdrm.h)
description: Creates an XrML right that will define a right granted to a user or group.
helpviewer_keywords: ["DRMCreateRight","DRMCreateRight function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMCreateRight","rm.drmcreateright"]
old-location: rm\drmcreateright.htm
tech.root: rm
ms.assetid: 05074fbd-9268-41b4-a916-a932dc7a7858
ms.date: 12/05/2018
ms.keywords: DRMCreateRight, DRMCreateRight function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateRight, rm.drmcreateright
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMCreateRight
 - msdrm/DRMCreateRight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMCreateRight
---

# DRMCreateRight function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateRight</b> function creates an XrML right that will define a right granted to a user or group.

## -parameters

### -param wszRightName [in]

A pointer to a null-terminated Unicode string that contains the name of a user-defined or standard XrML (version 1.2) right. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/official-template-xrml">Official Template XrML</a>.

### -param pstFrom [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time, in UTC time, when this right will become valid. For more information, see Remarks. Both <i>pstFrom</i> and <i>pstUntil</i> must be specified, or both must be <b>NULL</b>.

### -param pstUntil [in]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the time, in UTC time, when this right will expire. For more information, see Remarks. Both <i>pstFrom</i> and <i>pstUntil</i> must be specified, or both must be <b>NULL</b>.

### -param cExtendedInfo [in]

The number of elements in the <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> arrays. If this parameter is zero, then both the <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> parameters must be <b>NULL</b>.

### -param pwszExtendedInfoName [in]

An array of null-terminated Unicode string pointers that contains the names of extended information data. Each name in this array must be unique. The <b>cExtendedInfo</b> parameter contains the number of elements in this array.

### -param pwszExtendedInfoValue [in]

An array of null-terminated Unicode string pointers that contains the values of the extended information items.  The <b>cExtendedInfo</b> parameter contains the number of elements in this array.

### -param phRight [out]

A pointer to a handle that receives the handle of the created right. This handle can be used with the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmaddrightwithuser">DRMAddRightWithUser</a> function to bind the right to a user. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Determining which rights a user can be granted is the responsibility of the application. The only right that Active Directory Rights Management Services enforces is EDIT, which grants the user the right to modify content.

A right can have any name that can be validly expressed in XML.

The <i>pstFrom</i> and <i>pstUntil</i> parameters specify the start and end validity times of the right. These parameters must either both be specified, or both be <b>NULL</b>. An application cannot set only one validity time.

One problem that can arise when creating licenses with short validity times is the problem of clock skew. <i>Clock skew</i> is when the publishing computer's clock and the end user's computer clock are not exactly aligned. Clock skew can cause attempts to exercise rights to fail. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/clock-skew">Clock Skew</a>.

The <i>pwszExtendedInfoName</i> and <i>pwszExtendedInfoValue</i> parameters are pointers to two parallel arrays that associate name-value pairs that hold additional right-specific information. These name-value pairs can specify any additional information you want, and they are retrieved by index number by using <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetrightextendedinfo">DRMGetRightExtendedInfo</a>. Extended information items are optional, but if a name or value is given, the corresponding item in the other array cannot be <b>NULL</b>.

Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosepubhandle">DRMClosePubHandle</a> to close the handle of the right created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/onlinesigning-getunsignedil-cpp">OnlineSigning_GetUnsignedIL.cpp</a>