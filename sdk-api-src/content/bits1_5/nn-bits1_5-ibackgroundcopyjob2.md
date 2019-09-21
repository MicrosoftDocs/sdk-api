---
UID: NN:bits1_5.IBackgroundCopyJob2
title: IBackgroundCopyJob2
author: windows-sdk-content
description: Retrieve reply data from an upload-reply job, determine the progress of the reply data transfer to the client, request command line execution, and provide credentials for proxy and remote server authentication requests.
old-location: bits\ibackgroundcopyjob2.htm
tech.root: Bits
ms.assetid: 9fd422ba-a68c-40e3-8b21-3077b271e58e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob2, IBackgroundCopyJob2 interface [BITS], IBackgroundCopyJob2 interface [BITS],described, _drz_ibackgroundcopyjob2, bits.ibackgroundcopyjob2, bits1_5/IBackgroundCopyJob2
ms.topic: interface
f1_keywords: 
 - "bits1_5/IBackgroundCopyJob2"
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2
product: Windows
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
---

# IBackgroundCopyJob2 interface


## -description


Use the 
<b>IBackgroundCopyJob2</b> interface to retrieve reply data from an upload-reply job, determine the progress of the reply data transfer to the client, request command line execution, and provide credentials for proxy and remote server authentication requests.

The 
<b>IBackgroundCopyJob2</b> interface inherits from the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface. 

To get an 
<b>IBackgroundCopyJob2</b> interface pointer, call the <b>IBackgroundCopyJob::QueryInterface</b> method using <code>__uuidof(IBackgroundCopyJob2)</code> for the interface identifier. Use the 
<b>IBackgroundCopyJob2</b> interface pointer to call both the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> and 
<b>IBackgroundCopyJob2</b> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>. <b>IBackgroundCopyJob2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getnotifycmdline">GetNotifyCmdLine</a>
</td>
<td align="left" width="63%">
Retrieves the program that is executed when the job enters the error or transferred state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata">GetReplyData</a>
</td>
<td align="left" width="63%">
Retrieves an in-memory copy of the reply data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename">GetReplyFileName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file that contains the reply data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress">GetReplyProgress</a>
</td>
<td align="left" width="63%">
Retrieves progress information that indicates how many bytes of the reply file have been downloaded to the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-removecredentials">RemoveCredentials</a>
</td>
<td align="left" width="63%">
Removes credentials set by the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">SetCredentials</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials">SetCredentials</a>
</td>
<td align="left" width="63%">
Specifies the credentials to use for a proxy or server user authentication.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">SetNotifyCmdLine</a>
</td>
<td align="left" width="63%">
Specifies a program to execute when the job enters the error or transferred state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setreplyfilename">SetReplyFileName</a>
</td>
<td align="left" width="63%">
Specifies the name of the file to contain the reply data of an upload-reply job.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a>
 

 

