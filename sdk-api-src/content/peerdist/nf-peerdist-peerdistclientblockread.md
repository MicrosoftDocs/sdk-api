---
UID: NF:peerdist.PeerDistClientBlockRead
title: PeerDistClientBlockRead function
author: windows-driver-content
description: PeerDistClientBlockRead function reads content data blocks.
old-location: p2p\peerdistclientblockread.htm
old-project: P2PSdk
ms.assetid: ee64c0a8-7a07-4045-96fa-855b31c2e5b1
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PEERDIST_READ_TIMEOUT_DEFAULT, PEERDIST_READ_TIMEOUT_LOCAL_CACHE_ONLY, PeerDistClientBlockRead, PeerDistClientBlockRead function [Peer Networking], p2p.peerdistclientblockread, peerdist/PeerDistClientBlockRead
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PeerDist.dll
api_name:
-	PeerDistClientBlockRead
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistClientBlockRead function


## -description


The <b>PeerDistClientBlockRead</b> function reads content data blocks.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hContentHandle [in]

A content handle opened by <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a> function call.


### -param cbMaxNumberOfBytes

TBD


### -param pBuffer [in, out, optional]

Pointer to the buffer that receives the data from the local cache. This buffer must remain valid for the duration of the read operation. The caller must not use this buffer until the read operation is completed. If the <i>cbMaxNumberOfBytesToRead</i> argument is equal to 0, the <i>pBuffer</i> parameter can be <b>NULL</b>


### -param dwTimeoutInMilliseconds

Timeout value for the read, in milliseconds.  There are two special values that may be specified: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_READ_TIMEOUT_LOCAL_CACHE_ONLY"></a><a id="peerdist_read_timeout_local_cache_only"></a><dl>
<dt><b>PEERDIST_READ_TIMEOUT_LOCAL_CACHE_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that a read should  not cause any additional network traffic by contacting peers  or a Hosted Cache.

</td>
</tr>
<tr>
<td width="40%"><a id="PEERDIST_READ_TIMEOUT_DEFAULT"></a><a id="peerdist_read_timeout_default"></a><dl>
<dt><b>PEERDIST_READ_TIMEOUT_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Specifies the default timeout of 5 seconds.

</td>
</tr>
</table>
 


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. The start offset for read is specified by setting the <b>Offset</b> and <b>OffsetHigh</b> members of the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.  The <b>OffsetHigh</b> member should be set to the higher 32 bits of the start offset and the <b>Offset</b> member should be set to the lower 32 bits of the start offset.


#### - cbMaxNumberOfBytesToRead

The maximum number of bytes to read. If the <i>cbMaxNumberOfBytesToRead</i> is equal to 0, it indicates that the <b>PeerDistClientBlockRead</b> function is  querying the length of available consecutive content byes in the local cache at the current block read offset. The query will neither download content from the peers, nor return the count of bytes present in the peer cache.


## -returns



If the function succeeds, the return value is <b>ERROR_IO_PENDING</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i>   or <i>hContent</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The feature is disabled by Group Policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The service  is unavailable.

</td>
</tr>
</table>
 




## -remarks



<b>PeerDistClientBlockRead</b> queues the read and immediately returns to the caller.  As a result, multiple reads can be issued simultaneously.
<b>PeerDistClientBlockRead</b>  will complete a read as soon as any data is available and will not wait for the buffer to fill completely.


If the <b>PeerDistClientBlockRead</b> function operation completes successfully, the <b>Offset</b> and <b>OffsetHigh</b> fields of the <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure will be populated with the <b>ULONGLONG</b> offset at which the read started.  The OffsetHigh member will be set to the higher 32 bits of the offset and the Offset member will be set to the lower 32 bits of the offset. <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> will populate <i>lpNumberOfBytesTransferred</i> with the number of bytes transferred. In the event the caller is using a completion port to process Peer Distribution API completions then the <i>lpNumberOfBytes</i> argument of <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> will be populated with the number of bytes transferred. 

If the <i>cbMaxNumberOfBytesToRead</i> argument is equal to 0, and the <b>PeerDistClientBlockRead</b> function completes successfully, the number of bytes transferred (obtained via either <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> or <a href="http://go.microsoft.com/fwlink/p/?linkid=131012">GetOverlappedResult</a>) will contain the actual length of  content available in the local cache.

When this API completes with  error values <b>PEERDIST_ERROR_MISSING_DATA</b> or <b>ERROR_TIMEOUT</b>, the <b>Offset</b> and <b>OffsetHigh</b> fields of the <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure specify the <b>ULONGLONG</b> offset at which the missing data range begins.  The OffsetHigh member will be set to the higher 32 bits of the offset and the Offset member will be set to the lower 32 bits of the offset. This missing data range is the start offset (relative to start of the content) and length, in bytes, which needs to be retrieved from an alternate source, like the original content server. In order to allow the Peer Distribution service to satisfy the same read in the future, add this data to the local cache by calling PeerDistClientAddData.  The length of the missing data range is specified by the number of bytes transferred (obtained via <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> or <a href="http://go.microsoft.com/fwlink/p/?linkid=131012">GetOverlappedResult</a>).

It is important to note that the missing data range can start at any offset in the content and be any length up to the end of the content. In the event the content information passed to <a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a> was generated in response to a range request, then the missing data range will be constrained to the range request bounds. This occurs when the call to <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a> on the content server specified an offset and a length which was a sub-range of the content as a whole. A completion with <b>ERROR_NO_MORE</b> in this case indicates that the read offset is outside of the sub-range of the content.

<h3><a id="Range_Requests"></a><a id="range_requests"></a><a id="RANGE_REQUESTS"></a>Range Requests</h3>
If a client is interested in only a portion of the original content, a range request can be used to retrieve that portion. A range request contains an offset and length of the original content. The size of the content information is directly proportional to the size of the content requested.


<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a> supports generating content information for a range request via the ullContentOffset and <i>cbContentLength</i> parameters. The <i>ullContentOffset</i> parameter represents the offset in the original content where the range begins and <i>cbContentLength</i> represents the length of the range.

Once a client obtains content information representing a particular content range, that content information works seamlessly with the  <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>, <a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a> and <a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a> APIs.  The content information can be passed to <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a> and will associate the <b>PEERDIST_CONTENT_HANDLE</b> with the content range.  <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> is constrained by the <i>ullContentOffset</i> offset and <i>cbContentLength</i> length specified in the server side call to <a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a>.  <b>PeerDistClientStreamRead</b> will begin at <i>ullContentOffset</i> and will complete with the error code <b>PEERDIST_ERROR_NO_MORE</b> when the end of the content range is reached at <i>ullContentOffset</i> + <i>cbContentLength</i>.  <b>PeerDistClientBlockRead</b> will complete with the error code <b>PEERDIST_ERROR_NO_MORE</b> if the offset specified in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> parameter is less than <i>ullContentOffset</i> or greater than <i>ullContentOffset</i> + <i>cbContentLength</i>.  <b>PeerDistClientStreamRead</b> and <b>PeerDistClientBlockRead</b> both limit the amount of missing data reported to the content range specified in the content information associated with the <b>PEERDIST_CONTENT_HANDLE</b>.  For example, if the content information represents only the first half of the content, missing data will be limited to the first half of the content.  In all other respects, <b>PeerDistClientBlockRead</b> and <b>PeerDistClientStreamRead</b> work with content ranges in exactly the same manner in which they work with the content as a whole.

A client can use <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> or  <b>PeerDistClientBlockRead</b> to retrieve the content from the offset specified by the <i>ullContentOffset</i> up to the length specified by <i>cbContentLength</i> in the <a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a> call. Both  <b>PeerDistClientStreamRead</b> and  <b>PeerDistClientBlockRead</b> will complete with <b>PEERDIST_ERROR_NO_MORE</b> if the client tries to read beyond the range specified by the <i>ullContentOffset</i> and <i>cbContentLength</i>. Additionally, <b>PeerDistClientBlockRead</b> will also complete with the error code <b>PEERDIST_ERROR_NO_MORE</b> if the offset specified in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> parameter is less than <i>ullContentOffset</i>

 
If the read cannot not be completed from either the local cache or the peer cache, both <a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a> and <b>PeerDistClientBlockRead</b> will report <b>PEERDIST_ERROR_MISSING_DATA</b>. When using the ranged content information, <b>PeerDistClientStreamRead</b> will report a missing data from the start offset of the range up to the end of the range. <b>PeerDistClientBlockRead</b> will report  missing data from start offset of the range up to the end of the range.


<a href="https://msdn.microsoft.com/f1fdd398-ed84-4819-b0e8-e9b653bd6848">PeerDistClientAddData</a> allows content data to be added even if it lies outside the content range.  This extended data will be validated after the corresponding content information has been added to the local cache.  Once validated, it becomes available to peers.  In other words, if a client adds only content information for the first half of content, <b>PeerDistClientAddData</b> still allows the client to add data for the entire content.  However, the second half of the content will not be validated until the corresponding content information for the second half has been added.  No other Peer Distribution APIs are affected by range requests.




## -see-also




<a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>



<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

