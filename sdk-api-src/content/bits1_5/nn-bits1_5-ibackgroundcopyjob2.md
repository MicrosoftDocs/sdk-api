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

# IBackgroundCopyJob2 interface


## -description



			Use the 
<b>IBackgroundCopyJob2</b> interface to retrieve reply data from an upload-reply job, determine the progress of the reply data transfer to the client, request command line execution, and provide credentials for proxy and remote server authentication requests.

The 
<b>IBackgroundCopyJob2</b> interface inherits from the 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> interface. 

To get an 
<b>IBackgroundCopyJob2</b> interface pointer, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob2)</code> for the interface identifier. Use the 
<b>IBackgroundCopyJob2</b> interface pointer to call both the 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> and 
<b>IBackgroundCopyJob2</b> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob2</b> interface inherits from <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>. <b>IBackgroundCopyJob2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62978315-e893-4617-8e6d-63bab8204913">GetNotifyCmdLine</a>
</td>
<td align="left" width="63%">
Retrieves the program that is executed when the job enters the error or transferred state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f29df35f-48c2-4837-9809-46bd04f08bfb">GetReplyData</a>
</td>
<td align="left" width="63%">
Retrieves an in-memory copy of the reply data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57f9245c-c1ae-4027-8e84-4926fa4861c3">GetReplyFileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file that contains the reply data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76509b1a-fdfb-4236-8554-f63282bfc1b6">GetReplyProgress</a>
</td>
<td align="left" width="63%">
Retrieves progress information that indicates how many bytes of the reply file have been downloaded to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbc6a05d-9e1f-4cc9-b28b-0874aafdfd7c">RemoveCredentials</a>
</td>
<td align="left" width="63%">
Removes credentials set by the 
<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">SetCredentials</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">SetCredentials</a>
</td>
<td align="left" width="63%">
Specifies the credentials to use for a proxy or server user authentication.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">SetNotifyCmdLine</a>
</td>
<td align="left" width="63%">
Specifies a program to execute when the job enters the error or transferred state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f8591a3-ecc2-497a-ac12-67e5862efde4">SetReplyFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the file to contain the reply data of an upload-reply job.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>
 

 

