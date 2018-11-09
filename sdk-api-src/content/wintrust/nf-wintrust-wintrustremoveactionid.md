---
UID: NF:wintrust.WintrustRemoveActionID
title: WintrustRemoveActionID function
author: windows-sdk-content
description: Removes an action added by the WintrustAddActionID function. This function has no associated import library.
old-location: security\wintrustremoveactionid.htm
tech.root: seccrypto
ms.assetid: d1c84b69-4886-4cb4-99c5-294bd9d8228b
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: HTTPSPROV_ACTION, WINTRUST_ACTION_GENERIC_VERIFY, WINTRUST_ACTION_GENERIC_VERIFY_V2, WintrustRemoveActionID, WintrustRemoveActionID function [Security], security.wintrustremoveactionid, wintrust/WintrustRemoveActionID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WintrustRemoveActionID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WintrustRemoveActionID function


## -description


<p class="CCE_Message">[The <b>WintrustRemoveActionID</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WintrustRemoveActionID</b> function removes an action added by the <a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a> function. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param pgActionID [in]

A pointer to a <b>GUID</b> structure that identifies the action to remove and the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trust provider</a> that supports that action.

The WinTrust service is designed to work with trust providers implemented by third parties. Each trust provider provides its own unique set of action identifiers. For information about the action identifiers supported by a trust provider, see the documentation for that trust provider.

For example, Microsoft provides a Software Publisher Trust Provider that can establish the trustworthiness of software being downloaded from the Internet or some other public network. The Software Publisher Trust Provider supports the following action identifiers. These constants are defined in Softpub.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINTRUST_ACTION_GENERIC_VERIFY"></a><a id="wintrust_action_generic_verify"></a><dl>
<dt><b>WINTRUST_ACTION_GENERIC_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verify a certificate chain only.

</td>
</tr>
<tr>
<td width="40%"><a id="WINTRUST_ACTION_GENERIC_VERIFY_V2"></a><a id="wintrust_action_generic_verify_v2"></a><dl>
<dt><b>WINTRUST_ACTION_GENERIC_VERIFY_V2</b></dt>
</dl>
</td>
<td width="60%">
Verify a file or object using the Authenticode policy provider.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTPSPROV_ACTION"></a><a id="httpsprov_action"></a><dl>
<dt><b>HTTPSPROV_ACTION</b></dt>
</dl>
</td>
<td width="60%">
Verify an SSL/PCT connection through Internet Explorer.

</td>
</tr>
</table>
 


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a>
 

 

