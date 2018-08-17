---
UID: NF:msdrm.DRMDeleteLicense
title: DRMDeleteLicense function
author: windows-sdk-content
description: Deletes a license, client licensor certificate, revocation list, or issuance license template.
old-location: rm\drmdeletelicense.htm
old-project: adrms_sdk
ms.assetid: 596f9959-0beb-4051-87c4-b8704abd8fc0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMDeleteLicense, DRMDeleteLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDeleteLicense, rm.drmdeletelicense
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msdrm.h
req.include-header: 
req.redist: 
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
 - DRMDeleteLicense
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDeleteLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDeleteLicense</b> function deletes a license, client licensor certificate, revocation list, or issuance license template.


## -parameters




### -param hSession [in]

A handle to a license storage session or client session. You can use a  storage session handle to delete end-user licenses and revocation lists. You can use a client session handle to delete end-user licenses, rights account certificates,  client licensor certificates, and issuance license templates.

You can retrieve a handle to a license storage session by using   the <a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a> function. You can retrieve a handle to a client session by using the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function.


### -param wszLicenseId [in]

A pointer to a null-terminated string that contains the ID of the license or template to be deleted. The license ID can be found inside the <b>ID</b> element of the license XrML, by querying using the license querying functions and the <b>g_wszQUERY_CONTENTIDVALUE</b> constant. The template ID is a GUID. You can enumerate the GUIDs by calling the <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> function.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The AD RMS system does not check to determine whether out of date licenses or revocation lists are stored in the license store, even when acquiring a new license or revocation list for content already owned. Therefore, it is important to occasionally delete  licenses or certificates. This can be a time-consuming process, so it might be best to perform this action occasionally or during program idle time.

If you delete an <a href="https://msdn.microsoft.com/en-us/library/Aa362618(v=VS.85).aspx">end-user license</a>, this function will not automatically delete associated revocation lists.

If you delete a license by using the content  ID, the <i>hSession</i> parameter must be the handle of a client session.

License and certificate IDs can be enumerated by using <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>. If you already have the license or certificate you want to delete from the license store, you can query it for its ID (by using the <a href="https://msdn.microsoft.com/2ae65ed2-7702-4e9b-b986-68b83ebe8bf5">DRMParseUnboundLicense</a> and <a href="https://msdn.microsoft.com/4ddf2920-95ea-47be-a5dd-b68eee2de29e">DRMGetUnboundLicenseAttribute</a> functions with the <b>g_wszQUERY_IDVALUE</b> constant) and pass the value into this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a>



<a href="https://msdn.microsoft.com/4ddf2920-95ea-47be-a5dd-b68eee2de29e">DRMGetUnboundLicenseAttribute</a>



<a href="https://msdn.microsoft.com/2ae65ed2-7702-4e9b-b986-68b83ebe8bf5">DRMParseUnboundLicense</a>
 

 

