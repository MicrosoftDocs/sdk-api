---
UID: NF:msdrm.DRMGetBoundLicenseObject
title: DRMGetBoundLicenseObject function (msdrm.h)
description: Returns an object from a bound license.
helpviewer_keywords: ["DRMGetBoundLicenseObject","DRMGetBoundLicenseObject function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetBoundLicenseObject","rm.drmgetboundlicenseobject"]
old-location: rm\drmgetboundlicenseobject.htm
tech.root: rm
ms.assetid: d1be0668-fb5a-4541-92dc-34255ba3fdad
ms.date: 12/05/2018
ms.keywords: DRMGetBoundLicenseObject, DRMGetBoundLicenseObject function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetBoundLicenseObject, rm.drmgetboundlicenseobject
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
 - DRMGetBoundLicenseObject
 - msdrm/DRMGetBoundLicenseObject
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
 - DRMGetBoundLicenseObject
---

# DRMGetBoundLicenseObject function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetBoundLicenseObject</b> function returns an object from a bound license.

## -parameters

### -param hQueryRoot [in]

A handle to a license or license object, from a previous call to this function or from <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

### -param wszSubObjectType [in]

The type of XrML object to find. For more information, see Remarks.

### -param iWhich [in]

Zero-based index specifying which occurrence to retrieve.

### -param phSubObject [out]

A handle to the returned license object. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

There are many kinds of objects in a license, such as principals, rights, and access conditions. The Active Directory Rights Management system exposes an object-oriented interface to the underlying license XrML. This function, along with other <b>DRMGetBoundLicense_xxx</b> functions, allows an application to navigate this structure. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>. On first call, use the license handle itself as the query root.

On first call, this function takes the <b>DRMHANDLE</b> returned by <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>.

The <i>wszSubObjectType</i> parameter identifies an XrML type as shown in the following example. Using g_wszQUERY_OBJECTTYPE to query the XrML would return "Group Identity Licensor."


```cpp
<PRINCIPAL internal-id="1">
  <OBJECT type="Group Identity Licensor">
  <ID type="Group Identity">someone@example.com</ID> 
  <NAME>Pavel's Group Identity</NAME> 
  </OBJECT>
```


Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattribute">DRMGetBoundLicenseAttribute</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseattributecount">DRMGetBoundLicenseAttributeCount</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetboundlicenseobjectcount">DRMGetBoundLicenseObjectCount</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>