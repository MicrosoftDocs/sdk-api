---
UID: NF:msdrm.DRMSetApplicationSpecificData
title: DRMSetApplicationSpecificData function (msdrm.h)
description: Allows an issuance license to store arbitrary name-value pairs for use by the content-consuming application.
helpviewer_keywords: ["DRMSetApplicationSpecificData","DRMSetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetApplicationSpecificData","rm.drmsetapplicationspecificdata"]
old-location: rm\drmsetapplicationspecificdata.htm
tech.root: rm
ms.assetid: 659b2d73-1160-4e5a-8779-4bb272653c54
ms.date: 12/05/2018
ms.keywords: DRMSetApplicationSpecificData, DRMSetApplicationSpecificData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetApplicationSpecificData, rm.drmsetapplicationspecificdata
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
 - DRMSetApplicationSpecificData
 - msdrm/DRMSetApplicationSpecificData
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
 - DRMSetApplicationSpecificData
---

# DRMSetApplicationSpecificData function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetApplicationSpecificData</b> function allows an issuance license to store arbitrary name-value pairs for use by the content-consuming application.

## -parameters

### -param hIssuanceLicense [in]

A handle to an issuance license.

### -param fDelete [in]

A flag that indicates whether to add or delete this name-value pair.   <b>FALSE</b> indicates add; <b>TRUE</b> indicates delete.

### -param wszName [in]

The name of the data.

### -param wszValue [in]

The value of the data.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The values stored can be used to pass information to a consuming application, such as the version and name of the publishing application, contact information, or any other arbitrary information. Information is stored in a zero-based array and is retrieved by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetapplicationspecificdata">DRMGetApplicationSpecificData</a> function. This function is used both to store a value or delete a stored value, depending on the flag passed in.

One data pair that is processed by an Active Directory Rights Management Services (AD RMS) server is the string pair "Allow_Server_Editing"/"True". When an issuance license has this value pair, it will allow the service, or any trusted service, to reuse the content key. This allows an issuance license to be republished by using the AD RMS SOAP function <a href="/previous-versions/windows/desktop/adrms_sdk/-editissuancelicense">EditIssuanceLicense</a>. This function takes in an old issuance license (with this name-value pair) and a new unsigned issuance license, and puts the content key into the new license. The pair "Allow_Server_Editing"/"True" must be added to the new issuance license if you want to allow publishing again.

To prevent republishing, remove this name-value pair or do not include it (do not add the data item with the value "False").

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetapplicationspecificdata">DRMGetApplicationSpecificData</a>