---
UID: NF:msdrm.DRMSetMetaData
title: DRMSetMetaData function (msdrm.h)
description: Adds application-specific metadata to an issuance license.
helpviewer_keywords: ["DRMSetMetaData","DRMSetMetaData function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMSetMetaData","rm.drmsetmetadata"]
old-location: rm\drmsetmetadata.htm
tech.root: rm
ms.assetid: dcf95e9e-e2de-449e-a45a-4974094ecb7e
ms.date: 12/05/2018
ms.keywords: DRMSetMetaData, DRMSetMetaData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetMetaData, rm.drmsetmetadata
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
 - DRMSetMetaData
 - msdrm/DRMSetMetaData
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
 - DRMSetMetaData
---

# DRMSetMetaData function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetMetaData</b> function adds application-specific metadata to an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license to which the metadata will be added.

### -param wszContentId [in]

A pointer to a null-terminated Unicode string that uniquely identifies an item of content. The string can contain up to 40 characters plus a terminating null character. We recommend that you use <b>CoCreateGUID</b> to create a GUID. For more information about content IDs, see Remarks.

### -param wszContentIdType [in]

A pointer to a null-terminated Unicode string that specifies the type of identifier represented by the <i>wszContentId</i> parameter. Possible examples include "MSGUID", "ISBN", "CatalogNumber", and any other that you consider appropriate.

### -param wszSKUId [in, optional]

A pointer to a null-terminated Unicode string that contains an optional identifier. The string can contain up to 40 characters plus a terminating null character. The SKU ID is optional and allows for further content identification beyond that provided by the required content ID. If <i>wszSKUIdType</i> is specified, the <i>wszSKUId</i> parameter must be specified. Otherwise, it can be <b>NULL</b>.

### -param wszSKUIdType [in, optional]

A pointer to a null-terminated Unicode string that contains the type of identifier represented by the <i>wszSKUId</i> parameter. If <i>wszSKUId</i> is specified, the <i>wszSKUIdType</i> parameter must be specified. Otherwise, it can be <b>NULL</b>.

### -param wszContentType [in, optional]

A pointer to a null-terminated Unicode string that contains application-defined information about the content. Examples include "Financial Statement", "Source Code", "Office Document", and any other that you consider appropriate. This parameter is optional and can be <b>NULL</b>.

### -param wszContentName [in, optional]

A pointer to a null-terminated Unicode string that contains a display name for the content. This parameter is optional and can be <b>NULL</b>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>DRMSetMetaData</b> function is typically called after <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a> to set the content ID, name, and type in an issuance license for a specific item of content. The function is also called before <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a> or <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a>.

Content IDs are created and set in issuance licenses by a publishing application. For example, the application can call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a> to create a new issuance license. It can then call <b>CoCreateGUID</b> to  create a unique ID and <b>DRMSetMetaData</b> to associate the ID with the license. The AD RMS client places the ID in the &lt;WORK&gt; node of the issuance license as shown by the following diagram. For more information, see <a href="/previous-versions/windows/desktop/adrms_sdk/creating-an-issuance-license">Creating an Issuance License</a>.


``` syntax
<WORK>
   <OBJECT type="Microsoft Office Document">
      <ID type="MSGUID">{AEADA9BD84F246BD92385A611D624A02}</ID>
      <NAME>Microsoft Office Document</NAME>
   </OBJECT>
    .
    .
    .
</WORK>
```

After an issuance license has been created, a consuming application can use it to acquire an end–user license. For more information, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a>. The appropriate &lt;WORK&gt; nodes and their respective content IDs are copied from the issuance license to the end–user license.

Once an end–user license has been acquired, consuming applications internally use the content ID to bind to that license. For more information, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateboundlicense">DRMCreateBoundLicense</a>. Binding verifies the license chain, principals, and environment, and removes all rights that do not apply to the specified user. The bound license can then be used to decrypt protected content.

Finally, the content ID can be used to enumerate end–user licenses. For more information, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmenumeratelicense">DRMEnumerateLicense</a> and <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreatelicensestoragesession">DRMCreateLicenseStorageSession</a>. The content ID is used to locate an end–user license in the license store.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetmetadata">DRMGetMetaData</a>
