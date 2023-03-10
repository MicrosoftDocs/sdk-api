---
UID: NF:msdrm.DRMGetRightExtendedInfo
title: DRMGetRightExtendedInfo function (msdrm.h)
description: Retrieves custom name-value pairs attached to a right.
helpviewer_keywords: ["DRMGetRightExtendedInfo","DRMGetRightExtendedInfo function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetRightExtendedInfo","rm.drmgetrightextendedinfo"]
old-location: rm\drmgetrightextendedinfo.htm
tech.root: rm
ms.assetid: d228660a-3c20-403e-9a89-e35195b19f92
ms.date: 12/05/2018
ms.keywords: DRMGetRightExtendedInfo, DRMGetRightExtendedInfo function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetRightExtendedInfo, rm.drmgetrightextendedinfo
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
 - DRMGetRightExtendedInfo
 - msdrm/DRMGetRightExtendedInfo
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
 - DRMGetRightExtendedInfo
---

# DRMGetRightExtendedInfo function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>DRMGetRightExtendedInfo</b> method allows a user to add or retrieve arbitrary strings for a right. Applications can use this string to create generic conditions or add any other information associated with a right. These name-value pairs are added in <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a> as parallel arrays.

To enumerate the existing extended data values, iterate through the index numbers, starting at zero, until the function returns <b>E_DRM_NO_MORE_DATA</b>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>