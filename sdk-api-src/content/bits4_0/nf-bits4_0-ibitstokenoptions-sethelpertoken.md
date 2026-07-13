---
UID: NF:bits4_0.IBitsTokenOptions.SetHelperToken
title: IBitsTokenOptions::SetHelperToken (bits4_0.h)
description: Sets the helper token to impersonate the token of the COM client.
helpviewer_keywords: ["IBitsTokenOptions interface [BITS]","SetHelperToken method","IBitsTokenOptions.SetHelperToken","IBitsTokenOptions::SetHelperToken","SetHelperToken","SetHelperToken method [BITS]","SetHelperToken method [BITS]","IBitsTokenOptions interface","bits.ibitstokenoptions_sethelpertoken","bits4_0/IBitsTokenOptions::SetHelperToken"]
old-location: bits\ibitstokenoptions_sethelpertoken.htm
tech.root: Bits
ms.assetid: a31414b7-159e-4ce7-8d2d-02b62aa9759d
ms.date: 12/05/2018
ms.keywords: IBitsTokenOptions interface [BITS],SetHelperToken method, IBitsTokenOptions.SetHelperToken, IBitsTokenOptions::SetHelperToken, SetHelperToken, SetHelperToken method [BITS], SetHelperToken method [BITS],IBitsTokenOptions interface, bits.ibitstokenoptions_sethelpertoken, bits4_0/IBitsTokenOptions::SetHelperToken
req.header: bits4_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits4_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - IBitsTokenOptions::SetHelperToken
 - bits4_0/IBitsTokenOptions::SetHelperToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBitsTokenOptions.SetHelperToken
---

# IBitsTokenOptions::SetHelperToken


## -description

Sets the helper token to impersonate the token of the COM client. Because an application sets the token through COM impersonation, the token is not persistent and is valid only for the lifetime of a session. When the BITS service receives a log-off notification, the BITS service discards any helper tokens that are associated with the transfer job.



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

The impersonation level for the proxy blanket must be set to either <b>RPC_C_IMP_LEVEL_IMPERSONATE</b> or <b>RPC_C_IMP_LEVEL_DELEGATE</b>. For more information, see <a href="/windows/win32/com/security-blanket-negotiation">Security Blanket Negotiation</a>.

The cloaking flag should be set to <b>EOAC_DYNAMIC_CLOAKING</b>, which enables the COM server to use the thread token as the client's identity. For more information, see <a href="/windows/win32/com/cloaking">Cloaking</a> and <a href="/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities">EOLE_AUTHENTICATION_CAPABILITIES Enumeration</a>.

Older implementations effectively required that BITS users have  administrator privileges in order to set helper tokens. Starting with Windows 10, version 1607, non-administrator BITS users can use <b>IBitsTokenOptions::SetHelperToken</b> to set non-administrator helper tokens on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="/windows/desktop/Services/networkservice-account">NetworkService account</a>) to set helper tokens. 

Specifically, the implementation has been changed to allow users without administrator privileges to set helper tokens, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob::QueryInterface</a> call, and the helper token being set does not have the administrator SID (<b>DOMAIN_ALIAS_RID_ADMINS</b>) enabled.

## -see-also

<a href="/windows/desktop/api/bits4_0/nn-bits4_0-ibitstokenoptions">IBitsTokenOptions</a>
