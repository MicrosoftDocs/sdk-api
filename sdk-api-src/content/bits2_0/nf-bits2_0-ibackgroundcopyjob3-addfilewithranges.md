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

# IBackgroundCopyJob3::AddFileWithRanges


## -description


Adds a file to a download job and specifies the ranges of the file you want to download.


## -parameters




### -param RemoteUrl [in]

Null-terminated string that contains the name of the file on the server. For information on specifying the remote name, see the <b>RemoteName</b> member and Remarks section of the <a href="https://msdn.microsoft.com/bf5302e9-da8f-4c57-a998-fd49484e0584">BG_FILE_INFO</a> structure. 



					Starting with BITS 3.0, the SMB protocol is not supported for ranges.

<b>BITS 2.5 and 2.0:  </b>BITS supports the SMB protocol for ranges.


### -param LocalName [in]

Null-terminated string that contains the name of the file on the client. For information on specifying the local name, see the <b>LocalName</b> member and Remarks section of the <a href="https://msdn.microsoft.com/bf5302e9-da8f-4c57-a998-fd49484e0584">BG_FILE_INFO</a> structure.


### -param RangeCount [in]

Number of elements in <i>Ranges</i>. 


### -param Ranges [in]

Array of one or more <a href="https://msdn.microsoft.com/4ed20321-fb89-410b-906e-9f2c4366645a">BG_FILE_RANGE</a> structures that specify the ranges to download. Do not specify duplicate or overlapping ranges. 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
You can receive this error for one of the following reasons:

<ul>
<li>The <i>RangeCount</i> parameter is zero; you must specify one or more ranges.</li>
<li>The local or remote file name is not valid.</li>
<li>The remote file name uses an unsupported protocol.</li>
<li>The local file name was specified using a relative path.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You cannot call this method for upload or upload-reply jobs; only call this method for download jobs.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
User does not have permission to write to the specified directory on the client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_RANGE</b></dt>
</dl>
</td>
<td width="60%">
One of the ranges is invalid. For example, InitialOffset is set to <b>BG_LENGTH_TO_EOF</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_OVERLAPPING_RANGES</b></dt>
</dl>
</td>
<td width="60%">
You cannot specify duplicate or overlapping ranges. 

<div class="alert"><b>Note</b>  The ranges are sorted by the offset of the value, not the length.  If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.  For example, if  100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job. </div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_TOO_MANY_RANGES_IN_FILE</b></dt>
</dl>
</td>
<td width="60%">
The MaxRangesPerFile Group Policy setting determines how many ranges you can specify for a file. Adding these ranges exceeds the MaxRangesPerFile limit.

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



The ranges are written to the <i>LocalName</i> file in the order given. For example, if <i>Ranges</i> identifies bytes 100-199, 900-999, and 400-499 of the remote file, the local file will be 300 bytes long. Bytes 0-99 of the local file will contain bytes 100-199 of the remote file, bytes 100-199 of the local file will contain bytes 900-999 of the remote file, and bytes 200-299 of the local file will contain bytes 400-499 of the remote file.

The following table identifies possible error codes that can occur after you resume the job. These errors place the job in the BG_JOB_STATE_ERROR state.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td>BG_E_INVALID_SERVER_RESPONSE</td>
<td> BITS does not support servers that consolidate duplicate or overlapping ranges. </td>
</tr>
<tr>
<td>BG_E_INVALID_RANGE</td>
<td>One of the ranges is outside the boundaries of the remote file.</td>
</tr>
<tr>
<td>BG_E_INSUFFICIENT_RANGE_SUPPORT</td>
<td>The server does not support ranges.</td>
</tr>
</table>
 

BITS guarantees that the version of a file (based on file size and date, not content) that it transfers will be consistent; however, it does not guarantee that a set of files will be consistent. For example, if BITS is in the middle of downloading the second of two files in the job at the time that the files are updated on the server, BITS restarts the download of the second file; however, the first file is not downloaded again.

By default, a user can add up to 500 ranges for a file. This limit does not apply to administrators or service accounts. To change the default, set the <b>MaxRangesPerFile</b> group policy.

<b>Prior to Windows Vista:  </b>There is no limit on the number of files that a user can add to a job.

For better performance on Windows BranchCache-enabled file transfers, it is recommended that you set the range length to at least 400 bytes.


#### Examples

The following example shows how to call the <b>AddFileWithRanges</b> method to specify the ranges of a file to download. The example assumes the <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> variable, <i>pJob</i>, is valid.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    IBackgroundCopyJob *pJob;
    IBackgroundCopyJob3 *pJob3 = NULL;
    DWORD dwRangeCount = 3;                  //Number of elements in Ranges.
    BG_FILE_RANGE Ranges[] = {24, 17,        //Array of ranges to download (offset and length).
                              111, BG_LENGTH_TO_EOF,
                              83, 7
                             };

    //Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob3
    //interface pointer. The IBackgroundCopyJob3 interface contains the AddFileWithRanges method.
    hr = pJob-&gt;QueryInterface(__uuidof( IBackgroundCopyJob3 ), (void**)&amp;pJob3;);
    if (S_OK == hr)
    {
         pJob-&gt;Release(); //No longer need the IBackgoundCopyJob interface pointer.

         //Add a file to the job and specify the ranges from the file to download.
         hr = pJob3-&gt;AddFileWithRanges(L"&lt;REMOTENAMEGOESHERE&gt;", L"&lt;LOCALNAMEGOESHERE&gt;",
                                       dwRangeCount, Ranges);
         if (FAILED(hr))
         {
              //Handle error.
              //Returns E_NOTIMPL if not a download job.
              //Returns E_INVALIDARG if dwRangeCount is zero or the remote or local name is invalid.
              //Returns BG_E_INVALID_RANGE if one of the ranges is invalid.
              //Returns BG_E_OVERLAPPING_RANGES if you specify overlapping or duplicate ranges.
         }

          pJob3-&gt;Release(); //Release the interface if you are done with it.
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




<a href="https://msdn.microsoft.com/4ed20321-fb89-410b-906e-9f2c4366645a">BG_FILE_RANGE</a>



<a href="https://msdn.microsoft.com/2e0ea08e-5f97-45c9-9280-ce6c4dce7a17">IBackgroundCopyFile2::GetFileRanges</a>



<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">IBackgroundCopyJob::AddFile</a>
 

 

