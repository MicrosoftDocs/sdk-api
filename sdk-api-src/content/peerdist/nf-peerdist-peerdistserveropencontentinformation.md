---
UID: NF:peerdist.PeerDistServerOpenContentInformation
title: PeerDistServerOpenContentInformation function
author: windows-driver-content
description: PeerDistServerOpenContentInformation function opens a PEERDIST_CONTENTINFO_HANDLE. The client uses the handle to retrieve content information.
old-location: p2p\peerdistserveropencontentinformation.htm
old-project: P2PSdk
ms.assetid: 17b07141-2786-4192-ba7b-f3210c10aad4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerDistServerOpenContentInformation, PeerDistServerOpenContentInformation function [Peer Networking], p2p.peerdistserveropencontentinformation, peerdist/PeerDistServerOpenContentInformation
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
-	PeerDistServerOpenContentInformation
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistServerOpenContentInformation function


## -description


The <b>PeerDistServerOpenContentInformation</b> function opens a <b>PEERDIST_CONTENTINFO_HANDLE</b>. The client uses the handle to retrieve content information.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param cbContentIdentifier

The length, in bytes, of the content identifier.


### -param pContentIdentifier [in]

Pointer to a buffer that contains the content identifier.


### -param ullContentOffset

An offset from the beginning of the published content for which the content information handle is requested.


### -param cbContentLength

The length, in bytes, of the content (starting from the ullContentOffset) for which the content information is requested.


### -param hCompletionPort [in, optional]

A handle to the completion port used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param phContentInfo [out]

A handle  used to retrieve the content information.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

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
The <i>hPeerDist</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified content identifier data  is not published.

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
The service is unavailable.

</td>
</tr>
</table>
 




## -remarks



If function succeeds, the handle received by <i>phContentInfo</i> can be passed to the  
 <a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a> function to retrieve content information.
The  handle   must be closed via the <a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a> function.


If <i>ullContentOffset</i> and <i>cbContentLength</i> are both zero, then the content information for the whole content will be retrieved.




## -see-also




<a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a>
 

 

