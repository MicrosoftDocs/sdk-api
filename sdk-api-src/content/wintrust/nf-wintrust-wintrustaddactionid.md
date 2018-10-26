---
UID: NF:wintrust.WintrustAddActionID
title: WintrustAddActionID function
author: windows-sdk-content
description: Adds a trust provider action to the user's system.
old-location: security\wintrustaddactionid.htm
tech.root: seccrypto
ms.assetid: 3b282342-9c86-42fa-b745-e5194d2885dc
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: HTTPSPROV_ACTION, WINTRUST_ACTION_GENERIC_VERIFY, WINTRUST_ACTION_GENERIC_VERIFY_V2, WintrustAddActionID, WintrustAddActionID function [Security], security.wintrustaddactionid, wintrust/WintrustAddActionID
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
 - WintrustAddActionID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WintrustAddActionID function


## -description


<p class="CCE_Message">[The <b>WintrustAddActionID</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> and <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> technology  signature verification, use the .NET Framework.]

The <b>WintrustAddActionID</b> function adds a trust provider action to the user's system. This method should be called during the <a href="_com_dllregisterserver">DllRegisterServer</a> implementation of the trust provider. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

This method should be called only by a trust provider.


## -parameters




### -param pgActionID [in]

A pointer to a <b>GUID</b> structure that identifies the action to add  and the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trust provider</a> that supports that action.

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
 


### -param fdwFlags [in]

a value that determines whether registry errors are reported by this function. If <i>fdwFlags</i> is zero and this function experiences a registry error, the registry error will not be propagated to the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>  function. If <i>fdwFlags</i> is WT_ADD_ACTION_ID_RET_RESULT_FLAG (0x1) and this function experiences a registry error, the registry error will be propagated to the <b>GetLastError</b>  function.


### -param psProvInfo [in]

A pointer to the <a href="https://msdn.microsoft.com/0b2b482f-f087-4be7-b17f-91c287c3460d">CRYPT_REGISTER_ACTIONID</a> structure that defines the information for the trust provider.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b>  if the function fails.   If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function  to determine the reason for failure.  For information about any registry errors that this function may encounter, see the description for <i>fdwFlags</i>.




## -remarks



To remove an action that has been added by this function, call the  <a href="https://msdn.microsoft.com/d1c84b69-4886-4cb4-99c5-294bd9d8228b">WintrustRemoveActionID</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d1c84b69-4886-4cb4-99c5-294bd9d8228b">WintrustRemoveActionID</a>
 

 

