---
UID: NF:msdrm.DRMSetMetaData
title: DRMSetMetaData function
author: windows-sdk-content
description: Adds application-specific metadata to an issuance license.
old-location: rm\drmsetmetadata.htm
old-project: adrms_sdk
ms.assetid: dcf95e9e-e2de-449e-a45a-4974094ecb7e
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DRMSetMetaData, DRMSetMetaData function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetMetaData, rm.drmsetmetadata
ms.prod: windows
ms.technology: windows-sdk
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
 - DRMSetMetaData
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetMetaData function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <b>DRMSetMetaData</b> function is typically called after <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> to set the content ID, name, and type in an issuance license for a specific item of content. The function is also called before <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> or <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>.

Content IDs are created and set in issuance licenses by a publishing application. For example, the application can call <a href="https://msdn.microsoft.com/db2e9aa6-7021-4805-8fd7-94c8d02776b0">DRMCreateIssuanceLicense</a> to create a new issuance license. It can then call <b>CoCreateGUID</b> to  create a unique ID and <b>DRMSetMetaData</b> to associate the ID with the license. The AD RMS client places the ID in the &lt;WORK&gt; node of the issuance license as shown by the following diagram. For more information, see <a href="https://msdn.microsoft.com/495024be-5d97-4869-99f7-b68efb9e8039">Creating an Issuance License</a>.

<pre class="syntax" xml:space="preserve"><code>&lt;WORK&gt;
   &lt;OBJECT type="Microsoft Office Document"&gt;
      &lt;ID type="MSGUID"&gt;{AEADA9BD84F246BD92385A611D624A02}&lt;/ID&gt;
      &lt;NAME&gt;Microsoft Office Document&lt;/NAME&gt;
   &lt;/OBJECT&gt;
    .
    .
    .
&lt;/WORK&gt;</code></pre>
After an issuance license has been created, a consuming application can use it to acquire an end–user license. For more information, see <a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>. The appropriate &lt;WORK&gt; nodes and their respective content IDs are copied from the issuance license to the end–user license.

Once an end–user license has been acquired, consuming applications internally use the content ID to bind to that license. For more information, see <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>. Binding verifies the license chain, principals, and environment, and removes all rights that do not apply to the specified user. The bound license can then be used to decrypt protected content.

Finally, the content ID can be used to enumerate end–user licenses. For more information, see <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> and <a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a>. The content ID is used to locate an end–user license in the license store.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/bea3120a-11a2-42e9-bf1b-368cad25ede5">DRMGetMetaData</a>
 

 

