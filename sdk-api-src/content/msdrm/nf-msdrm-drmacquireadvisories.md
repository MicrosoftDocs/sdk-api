---
UID: NF:msdrm.DRMAcquireAdvisories
title: DRMAcquireAdvisories function
author: windows-sdk-content
description: Retrieves revocation lists required by a submitted license.
old-location: rm\drmacquireadvisories.htm
tech.root: AdRms_Sdk
ms.assetid: 42c58096-429c-4278-b9ab-8c5a91361af8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMAcquireAdvisories, DRMAcquireAdvisories function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAcquireAdvisories, rm.drmacquireadvisories
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
 - DRMAcquireAdvisories
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DRMAcquireAdvisories
: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMAcquireAdvisories function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAcquireAdvisories</b> function retrieves revocation lists required by a submitted license. Retrieved revocation lists are added to the user's permanent license store. A revocation list is a signed XrML document that specifies principals that have been revoked because they are no longer considered trustworthy or valid. These principals can include <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificates</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa362706(v=VS.85).aspx">machine certificates</a>, code-signing certificates, manifests, and server licensor certificates, among other things.


## -parameters




### -param hLicenseStorage [in]

A handle to a license storage session created by using the <a href="https://msdn.microsoft.com/6561b6df-373b-4bd3-9196-09ef945f8042">DRMCreateLicenseStorageSession</a> function.


### -param wszLicense [in]

A pointer to a null-terminated Unicode string that contains the license that requires a revocation list. This can be any license or certificate (or certificate chain or concatenated licenses) that supports revocation lists, including <a href="https://msdn.microsoft.com/en-us/library/Aa362618(v=VS.85).aspx">end-user licenses</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa362726(v=VS.85).aspx">rights account certificates</a>, or <a href="https://msdn.microsoft.com/en-us/library/Aa362374(v=VS.85).aspx">client licensor certificates</a>.


### -param wszURL [in, optional]

A pointer to a null-terminated Unicode string that contains an additional URL to query for advisories. This will be checked in addition to any URLs mentioned in the license passed in. This parameter can be set to <b>NULL</b>.


### -param pvContext [in]

A 32-bit, application-defined value that is sent in the <i>pvContext</i> parameter of the callback function. This value can be a pointer to data, a pointer to an event handle, or whatever else the custom callback function is designed to handle. For more information, see <a href="https://msdn.microsoft.com/41c200df-afbc-43a5-8046-d131fec3261a">Callback Prototype</a>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function retrieves advisory lists asynchronously. The URL where the revocation list is posted is stored in the license that is passed in, but it can be overridden by <i>wszURL</i>.

After an advisory list has been obtained, it must be registered by using <a href="https://msdn.microsoft.com/819a8471-e447-4a4d-ae52-5929350df2c8">DRMRegisterRevocationList</a>. It is simplest to enumerate all licenses in the license store by using <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> and then register each, rather than attempting to locate the item you just acquired.

You should periodically delete duplicate or outdated revocation lists from the license store by enumerating revocation lists. To enumerate revocation lists, call <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> with the <b>DRM_EL_EXPIRED</b> flag, and then call <a href="https://msdn.microsoft.com/596f9959-0beb-4051-87c4-b8704abd8fc0">DRMDeleteLicense</a>. Because enumerating and examining licenses can be time-consuming, an application might perform this task only periodically.

An application will be informed that a new revocation list must be acquired if the call to the <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a> function returns <b>E_DRM_BIND_REVOCATION_LIST_STALE</b> or <b>E_DRM_BIND_NO_APPLICABLE_REVOCATION_LIST</b>.

For more information about revocation lists and how to create them, see the Active Directory Rights Management Services deployment guide, which comes with <a href="http://go.microsoft.com/fwlink/p/?linkid=17673">Rights Management Services</a>.

The application callback function specified in the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function will be called with the <a href="https://msdn.microsoft.com/9984503c-9670-4ab1-acdb-460f420ee4e6">DRM_MSG_ACQUIRE_ADVISORY</a> message to provide status feedback.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/819a8471-e447-4a4d-ae52-5929350df2c8">DRMRegisterRevocationList</a>



<a href="https://msdn.microsoft.com/1e1a7cfc-8445-4d0c-bc45-310fa9364839">Revoking a Certificate</a>
 

 

