---
UID: NF:msdrm.DRMGetBoundLicenseAttribute
title: DRMGetBoundLicenseAttribute function (msdrm.h)
description: Retrieves a bound license attribute from the license XrML.
helpviewer_keywords: ["DRMGetBoundLicenseAttribute","DRMGetBoundLicenseAttribute function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetBoundLicenseAttribute","rm.drmgetboundlicenseattribute"]
old-location: rm\drmgetboundlicenseattribute.htm
tech.root: rm
ms.assetid: 715fb3e6-6b1e-4136-9c25-efcde2015d6f
ms.date: 12/05/2018
ms.keywords: DRMGetBoundLicenseAttribute, DRMGetBoundLicenseAttribute function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetBoundLicenseAttribute, rm.drmgetboundlicenseattribute
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
 - DRMGetBoundLicenseAttribute
 - msdrm/DRMGetBoundLicenseAttribute
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
 - DRMGetBoundLicenseAttribute
---

# DRMGetBoundLicenseAttribute function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetBoundLicenseAttribute</b> function retrieves a bound license attribute from the license XrML.

## -parameters

### -param hQueryRoot [in]

A handle to a root query object, from a previous call to this function or from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

### -param wszAttribute [in]

The attribute to retrieve.

### -param iWhich [in]

Zero-based index of the occurrence to retrieve.

### -param peEncoding [out]

Encoding type used.

### -param pcBuffer [in, out]

Size, in characters, of the attribute retrieved plus one for a terminating null character.

### -param pbBuffer [out]

Pointer to the attribute object.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The Active Directory Rights Management system exposes an object-oriented interface to the underlying license XrML. This function, along with other <b>DRMGetBoundLicense_xxx</b> functions, allows an application to navigate this structure.

Attributes hold information about an object, such as its name, issue time, or SKU value. To obtain attribute information, you must first determine the size of the buffer needed to hold the retrieved information by calling the function with <b>NULL</b> in the <i>pbBuffer</i> value. If the function succeeds and returns a value in <i>pcBuffer</i>, then allocate a properly sized buffer by using this value and call the function again, passing in to <i>pbBuffer</i> the allocated buffer to receive the value of the attribute.

An object can have several instances of an attribute with the same name. For example, there can be several authenticator type values in a license. In this case, it may be necessary to iterate through all the instances of an attribute by first calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattributecount">DRMGetBoundLicenseAttributeCount</a> to get a count of existing objects and then looping through all <i>iWhich</i> instances of the attribute, starting at zero and incrementing by one.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattributecount">DRMGetBoundLicenseAttributeCount</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobject">DRMGetBoundLicenseObject</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobjectcount">DRMGetBoundLicenseObjectCount</a>