---
UID: NF:msdrm.DRMGetUnboundLicenseObject
title: DRMGetUnboundLicenseObject function (msdrm.h)
description: Retrieves an object of a specified type in an unbound license.
helpviewer_keywords: ["DRMGetUnboundLicenseObject","DRMGetUnboundLicenseObject function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMGetUnboundLicenseObject","rm.drmgetunboundlicenseobject"]
old-location: rm\drmgetunboundlicenseobject.htm
tech.root: rm
ms.assetid: d3e03d62-5202-4969-a4c7-5fbf89070436
ms.date: 12/05/2018
ms.keywords: DRMGetUnboundLicenseObject, DRMGetUnboundLicenseObject function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetUnboundLicenseObject, rm.drmgetunboundlicenseobject
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
 - DRMGetUnboundLicenseObject
 - msdrm/DRMGetUnboundLicenseObject
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
 - DRMGetUnboundLicenseObject
---

# DRMGetUnboundLicenseObject function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetUnboundLicenseObject</b> function retrieves an object of a specified type in an unbound license.

## -parameters

### -param hQueryRoot [in]

A handle to a license or object in the license, created using <b>DRMGetUnboundLicenseObject</b> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmparseunboundlicense">DRMParseUnboundLicense</a>.

### -param wszSubObjectType [in]

Name of the object to find.

### -param iIndex [in]

Zero-based index indicating which instance to retrieve, if more than one exists.

### -param phSubQuery [out]

The retrieved object. Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosehandle">DRMCloseHandle</a> to close the  handle.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Each object can have several instances within a license. A license may contain many rights objects, for example. In this case, it may be necessary to iterate through all the objects in this class by first calling <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobjectcount">DRMGetUnboundLicenseObjectCount</a> to get a count of existing objects, and then looping through all instances, starting at zero and incrementing the <i>iWhich</i> value by one. If a specific object is sought, each retrieved object can be queried for its attributes, such as its name.

This query will search only at the level immediately below the passed in object. So, for example, if the root license handle is passed in and the attribute to find is g_wszQUERY_OWNER, the query will find nothing because the OWNER object appears at the second level or deeper (counting the license root as level 0).

The <i>wszSubObjectType</i> parameter identifies an XrML node value as shown in the following example. Using g_wszQUERY_OBJECTTYPE in a query would return "Group Identity Licensor." The only object you can query for in an issuance license is g_wszQUERY_DISTRIBUTIONPOINT.


```cpp
<PRINCIPAL internal-id="1">
  <OBJECT type="Group Identity Licensor">
  <ID type="Group Identity">someone@example.com</ID>
  <NAME>Pavel's Group Identity</NAME>
  </OBJECT>
```


Call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclosequeryhandle">DRMCloseQueryHandle</a>  to close the object handle created by calling this function.

## -see-also

<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattribute">DRMGetUnboundLicenseAttribute</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseattributecount">DRMGetUnboundLicenseAttributeCount</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetunboundlicenseobjectcount">DRMGetUnboundLicenseObjectCount</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/querying-licenses">Querying Licenses</a>