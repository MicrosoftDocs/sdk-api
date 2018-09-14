---
UID: NF:bits4_0.IBitsTokenOptions.GetHelperTokenFlags
title: IBitsTokenOptions::GetHelperTokenFlags
author: windows-sdk-content
description: Returns the usage flags for a token that is associated with a BITS transfer job.
old-location: bits\ibitstokenoptions_gethelpertokenflags.htm
tech.root: Bits
ms.assetid: d00596bf-7695-4a5e-8d13-4700876fdef6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BG_TOKEN_LOCAL_FILE, BG_TOKEN_NETWORK, GetHelperTokenFlags, GetHelperTokenFlags method [BITS], GetHelperTokenFlags method [BITS],IBitsTokenOptions interface, IBitsTokenOptions interface [BITS],GetHelperTokenFlags method, IBitsTokenOptions.GetHelperTokenFlags, IBitsTokenOptions::GetHelperTokenFlags, bits.ibitstokenoptions_gethelpertokenflags, bits4_0/IBitsTokenOptions::GetHelperTokenFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBitsTokenOptions.GetHelperTokenFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
---

# IBitsTokenOptions::GetHelperTokenFlags


## -description


Returns the usage flags for a token that is associated with a BITS transfer job.


## -parameters




### -param pFlags [out]

Specifies the usage flag to return. This parameter must be set to one of the following values:

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
An application is required to call the <a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a> method to allow the credentials to be sent over HTTP.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Older implementations effectively required that BITS users have  administrator privileges in order to get helper token flags with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to get helper token usage flags on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="https://msdn.microsoft.com/f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to get helper token flags, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob::QueryInterface</a> call.




## -see-also




<a href="https://msdn.microsoft.com/8496c27b-68d8-4709-b8a6-6ffa17c886df">IBitsTokenOptions</a>
 

 

