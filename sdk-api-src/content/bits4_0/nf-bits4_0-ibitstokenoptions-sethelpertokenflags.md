---
UID: NF:bits4_0.IBitsTokenOptions.SetHelperTokenFlags
title: IBitsTokenOptions::SetHelperTokenFlags
author: windows-sdk-content
description: Sets the usage flags for a token that is associated with a BITS transfer job.
old-location: bits\ibitstokenoptions_sethelpertokenflags.htm
old-project: bits
ms.assetid: bee8fda2-ec11-4969-be81-57a8b4177a1c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BG_TOKEN_LOCAL_FILE, BG_TOKEN_NETWORK, IBitsTokenOptions interface [BITS],SetHelperTokenFlags method, IBitsTokenOptions.SetHelperTokenFlags, IBitsTokenOptions::SetHelperTokenFlags, SetHelperTokenFlags, SetHelperTokenFlags method [BITS], SetHelperTokenFlags method [BITS],IBitsTokenOptions interface, bits.ibitstokenoptions_sethelpertokenflags, bits4_0/IBitsTokenOptions::SetHelperTokenFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits4_0.h
req.include-header: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
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
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBitsTokenOptions.SetHelperTokenFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
An application is required to call <a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials (..., NULL, NULL)</a> to allow the credentials to be sent over HTTP.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The helper token usage flags specify which resources are to be accessed using the helper token’s security context. BITS will access all other resources using the job owner’s security context. For example, the client certificate is accessed by using the job owner identity.

If a client certificate is specified and the owner of the BITS job is not the LocalSystem account, setting the <i>UsageFlag</i> parameter to <b>BG_TOKEN_NETWORK</b> will cause the job to fail with the error code 0x80072f9a (<b>ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY</b>). 

Older implementations effectively required that BITS users have  administrator privileges in order to set helper token usage flags with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to set non-administrator helper token usage flags on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="https://msdn.microsoft.com/f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to set helper token usage flags, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob::QueryInterface</a> call, and the helper token that is currently set (if any) does not have the administrator SID (<b>DOMAIN_ALIAS_RID_ADMINS</b>) enabled.




## -see-also




<a href="https://msdn.microsoft.com/8496c27b-68d8-4709-b8a6-6ffa17c886df">IBitsTokenOptions</a>
 

 

