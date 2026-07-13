---
UID: NF:bits4_0.IBitsTokenOptions.SetHelperTokenFlags
title: IBitsTokenOptions::SetHelperTokenFlags (bits4_0.h)
description: Sets the usage flags for a token that is associated with a BITS transfer job.
helpviewer_keywords: ["BG_TOKEN_LOCAL_FILE","BG_TOKEN_NETWORK","IBitsTokenOptions interface [BITS]","SetHelperTokenFlags method","IBitsTokenOptions.SetHelperTokenFlags","IBitsTokenOptions::SetHelperTokenFlags","SetHelperTokenFlags","SetHelperTokenFlags method [BITS]","SetHelperTokenFlags method [BITS]","IBitsTokenOptions interface","bits.ibitstokenoptions_sethelpertokenflags","bits4_0/IBitsTokenOptions::SetHelperTokenFlags"]
old-location: bits\ibitstokenoptions_sethelpertokenflags.htm
tech.root: Bits
ms.assetid: bee8fda2-ec11-4969-be81-57a8b4177a1c
ms.date: 12/05/2018
ms.keywords: BG_TOKEN_LOCAL_FILE, BG_TOKEN_NETWORK, IBitsTokenOptions interface [BITS],SetHelperTokenFlags method, IBitsTokenOptions.SetHelperTokenFlags, IBitsTokenOptions::SetHelperTokenFlags, SetHelperTokenFlags, SetHelperTokenFlags method [BITS], SetHelperTokenFlags method [BITS],IBitsTokenOptions interface, bits.ibitstokenoptions_sethelpertokenflags, bits4_0/IBitsTokenOptions::SetHelperTokenFlags
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
 - IBitsTokenOptions::SetHelperTokenFlags
 - bits4_0/IBitsTokenOptions::SetHelperTokenFlags
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
 - IBitsTokenOptions.SetHelperTokenFlags
---

# IBitsTokenOptions::SetHelperTokenFlags


## -description

Sets the usage flags for a token that is associated with a BITS transfer job.

## -parameters

### -param UsageFlags

Specifies the usage flag. This parameter must be set to one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_TOKEN_LOCAL_FILE"></a><a id="bg_token_local_file"></a><dl>
<dt><b>BG_TOKEN_LOCAL_FILE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
If this flag is specified, the helper token is used

<ul>
<li>To open the local file of an upload job</li>
<li>To create or rename the temporary file of a download job</li>
<li>To create or rename the reply file of an upload-reply job</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="BG_TOKEN_NETWORK"></a><a id="bg_token_network"></a><dl>
<dt><b>BG_TOKEN_NETWORK</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
If this flag is specified, the helper token is used

<ul>
<li>To open the remote file of a Server Message Block (SMB) upload or download job</li>
<li>In response to an HTTP server or proxy challenge for implicit NTLM or Kerberos credentials</li>
</ul>
An application is required to call <a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">IBackgroundCopyJob2::SetCredentials (..., NULL, NULL)</a> to allow the credentials to be sent over HTTP.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The helper token usage flags specify which resources are to be accessed using the helper token’s security context. BITS will access all other resources using the job owner’s security context. For example, the client certificate is accessed by using the job owner identity.

If a client certificate is specified and the owner of the BITS job is not the LocalSystem account, setting the <i>UsageFlag</i> parameter to <b>BG_TOKEN_NETWORK</b> will cause the job to fail with the error code 0x80072f9a (<b>ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY</b>). 

Older implementations effectively required that BITS users have  administrator privileges in order to set helper token usage flags with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to set non-administrator helper token usage flags on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="/windows/desktop/Services/networkservice-account">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to set helper token usage flags, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob::QueryInterface</a> call, and the helper token that is currently set (if any) does not have the administrator SID (<b>DOMAIN_ALIAS_RID_ADMINS</b>) enabled.

## -see-also

<a href="/windows/desktop/api/bits4_0/nn-bits4_0-ibitstokenoptions">IBitsTokenOptions</a>