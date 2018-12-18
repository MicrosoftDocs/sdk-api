---
UID: NF:bits2_0.IBackgroundCopyJob3.ReplaceRemotePrefix
title: IBackgroundCopyJob3::ReplaceRemotePrefix
author: windows-sdk-content
description: Replaces the beginning text of all remote names in the download job with the specified string.
old-location: bits\ibackgroundcopyjob3_replaceremoteprefix.htm
tech.root: bits
ms.assetid: 5ea62d29-c40e-4bd2-b22a-fce2d9f4eecf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyJob3 interface [BITS],ReplaceRemotePrefix method, IBackgroundCopyJob3.ReplaceRemotePrefix, IBackgroundCopyJob3::ReplaceRemotePrefix, ReplaceRemotePrefix, ReplaceRemotePrefix method [BITS], ReplaceRemotePrefix method [BITS],IBackgroundCopyJob3 interface, bits.ibackgroundcopyjob3_replaceremoteprefix, bits2_0/IBackgroundCopyJob3::ReplaceRemotePrefix
ms.topic: method
req.header: bits2_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2,KB842773 on  Windows Server 2003,  and Windows XP
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits2_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx3.dll
api_name:
 - IBackgroundCopyJob3.ReplaceRemotePrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob3::ReplaceRemotePrefix


## -description


Replaces the beginning text of all  remote names in the download job with the specified string.


## -parameters




### -param OldPrefix [in]

Null-terminated string that identifies the  text to  replace in the remote name. The text must start at the beginning of the remote name.


### -param NewPrefix [in]

Null-terminated string that contains the replacement text.


## -returns



This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No matches found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Applying  <i>NewPrefix</i> creates an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).

You can also receive this return code if the <i>OldPrefix</i> or <i>NewPrefix</i> is an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You cannot call this method for upload or upload-reply jobs; call this method only for download jobs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the job cannot be <b>BG_JOB_STATE_CANCELLED</b> or <b>BG_JOB_STATE_ACKNOWLEDGED</b>.

</td>
</tr>
</table>
 




## -remarks



Typically, you use this method to change the server portion of the remote name when the server is unavailable or to let  roaming users connect to the closest server. This method changes all matching remote names in the job. To change the remote name of a specific file, use the <a href="https://msdn.microsoft.com/6dd33b7d-4317-4eb5-aae4-83d3f4416bf9">IBackgroundCopyFile2::SetRemoteName</a> method.

The <b>ReplaceRemotePrefix</b> method performs a case-sensitive search of all the  remote names in the job. If the beginning text of the remote name matches the string in <i>OldPrefix</i>, BITS replaces the text with the string found in <i>NewPrefix</i>. For example, to change "http://Server/Path/File.ext" to "http://NewServerName/Path/File.ext", set <i>OldPrefix</i> to "http://Server" and <i>NewPrefix</i> to "http://NewServerName". Note that BITS does not perform locale conversions in the search.

If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), BITS restarts the download. Otherwise, the transfer resumes from the same position on the new server. BITS does not restart already transferred files. 

You can use this method to change protocols. However, the resulting URL may not be well formed. For example, changing from \\Server\Dir\File.ext to http://Server\Dir\File.ext may not resolve. Consider using the <a href="https://msdn.microsoft.com/6dd33b7d-4317-4eb5-aae4-83d3f4416bf9">IBackgroundCopyFile2::SetRemoteName</a> method instead.

Note that this method may not find URLs to change if you called the <a href="https://msdn.microsoft.com/afac84cb-28ab-4c80-ab39-eefe450ae3e5">IBackgroundCopyJobHttpOptions::SetSecurityFlags</a> method and set the <b>BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT</b> flag. This policy changes the original URL to the final, redirected URL if the URL is redirected.


#### Examples

The following example shows how to call the <b>ReplaceRemotePrefix</b> method to change the server name of a URL. The example assumes the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> variable, <i>pJob</i>, is valid and the job contains one or more files.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>     IBackgroundCopyJob *pJob;
     IBackgroundCopyJob3 *pJob3 = NULL;

     //Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob3
     //interface pointer. The IBackgroundCopyJob3 interface contains the ReplaceRemotePrefix method.
     hr = pJob-&gt;QueryInterface(__uuidof( IBackgroundCopyJob3 ), (void**)&amp;pJob3;);
     if (S_OK == hr)
     {
          pJob-&gt;Release(); //No longer need the IBackgoundCopyJob interface pointer.

          //Identify the old and new remote name text. For example, "http://oldservername" and 
          //"http://newservername". For SMB, specify "\\\\oldservername" and "\\\\newservername".
          hr = pJob3-&gt;ReplaceRemotePrefix(L"&lt;OLDSERVERNAMEGOESHERE&gt;", L"&lt;NEWSERVERNAMEGOESHERE&gt;");
          if (S_FALSE == hr)
          {
               wprintf(L"The job does not contain files with a remote name that matches the prefix.\n");
          }
          else if (FAILED(hr))
          {
               //Handle error.
               //Returns E_NOTIMPL if not a download job.
               //Returns E_INVALIDARG if new prefix is empty or the resulting URL is invalid.
          }

          pJob3-&gt;Release();
     }
     else
     {
          //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
          //running on the computer is less than BITS 2.0.
     }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6dd33b7d-4317-4eb5-aae4-83d3f4416bf9">IBackgroundCopyFile2::SetRemoteName</a>



<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>
 

 

