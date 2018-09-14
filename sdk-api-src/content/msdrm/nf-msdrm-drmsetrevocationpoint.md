---
UID: NF:msdrm.DRMSetRevocationPoint
title: DRMSetRevocationPoint function
author: windows-sdk-content
description: Sets a refresh rate and location to obtain a revocation list.
old-location: rm\drmsetrevocationpoint.htm
tech.root: AdRms_Sdk
ms.assetid: a9f4ff8d-1b9f-46f4-8a69-5957d4b2aefb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DRMSetRevocationPoint, DRMSetRevocationPoint function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetRevocationPoint, rm.drmsetrevocationpoint
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMSetRevocationPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetRevocationPoint function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetRevocationPoint</b> function sets a refresh rate and location to obtain a revocation list.


## -parameters




### -param hIssuanceLicense [in]

A handle to an issuance license.


### -param fDelete [in]

Flag indicating whether the existing item should be deleted:    <b>TRUE</b> indicates it should be deleted; <b>FALSE</b> indicates it should be added.


### -param wszId [in]

ID of the revocation authority posting the revocation list. This must match the ID given in the <b>ISSUER</b> node of the revocation list.


### -param wszIdType [in]

Type of ID used by <i>wszId</i>.


### -param wszURL [in]

URL of revocation file list.


### -param pstFrequency [in]

How often the list must be updated.


### -param wszName [in]

Optional human-readable name for a revocation list site.


### -param wszPublicKey [in]

Public key of key pair used to sign and verify the revocation list.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A revocation list can revoke end-user licenses, server licensor certificates, or almost anything else with an identifying GUID. For a list of the items that can be revoked, see <a href="https://msdn.microsoft.com/ec8ec1d8-5c43-4f6d-93bd-7875c110cac0">Revocation</a>. The URL provided should refer to the list file itself. The rights management system handles checking for a valid revocation list. This function should only be called once, since subsequent calls will overwrite the previous revocation point in the issuance license.

The public key must be a base-64 encoded string.

Note that if there is no revocation point set in the license, the license can still be revoked by a revocation list signed by the issuer of the license.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/11197e77-0b7f-4972-83a1-a82aa5cef0dd">DRMGetRevocationPoint</a>



<a href="https://msdn.microsoft.com/1e1a7cfc-8445-4d0c-bc45-310fa9364839">Revoking a Certificate</a>
 

 

