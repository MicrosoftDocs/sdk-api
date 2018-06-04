---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBitsTokenOptions::SetHelperToken


## -description


Sets the helper token to impersonate the token of the COM client. Because an application sets the token through COM impersonation, the token is not persistent and is valid only for the lifetime of a session. When the BITS service receives a log-off notification, the BITS service discards any helper tokens that are associated with the transfer job.


## -parameters






## -returns



The following value might be returned:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_FAILEDTOIMPERSONATE</b></dt>
<dt>0x80010123</dt>
</dl>
</td>
<td width="60%">
COM settings on the client do not allow impersonate-level access to the client token.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
<ul>
<li>In versions prior to Windows 10, version 1607, the job is not owned by an administrator. In those versions of Windows, only administrator-owned jobs may set helper tokens.
</li>
<li>In Windows 10, version 1607 and newer versions, this error indicates that the helper token has administrator privileges, but the caller does not have administrator privileges.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



The helper token does not need to represent an administrator.

The impersonation level for the proxy blanket must be set to either <b>RPC_C_IMP_LEVEL_IMPERSONATE</b> or <b>RPC_C_IMP_LEVEL_DELEGATE</b>. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=146948">Security Blanket Negotiation</a>.

The cloaking flag should be set to <b>EOAC_DYNAMIC_CLOAKING</b>, which enables the COM server to use the thread token as the client's identity. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=158904">Cloaking</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=158905">EOLE_AUTHENTICATION_CAPABILITIES Enumeration</a>.

Older implementations effectively required that BITS users have  administrator privileges in order to set helper tokens. Starting with Windows 10, version 1607, non-administrator BITS users can use <b>IBitsTokenOptions::SetHelperToken</b> to set non-administrator helper tokens on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="https://msdn.microsoft.com/f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7">NetworkService account</a>) to set helper tokens. 

Specifically, the implementation has been changed to allow users without administrator privileges to set helper tokens, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob::QueryInterface</a> call, and the helper token being set does not have the administrator SID (<b>DOMAIN_ALIAS_RID_ADMINS</b>) enabled.




## -see-also




<a href="https://msdn.microsoft.com/8496c27b-68d8-4709-b8a6-6ffa17c886df">IBitsTokenOptions</a>
 

 

