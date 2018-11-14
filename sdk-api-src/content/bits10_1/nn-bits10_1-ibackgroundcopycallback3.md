---
UID: NN:bits10_1.IBackgroundCopyCallback3
title: IBackgroundCopyCallback3
author: windows-sdk-content
description: Clients implement the IBackgroundCopyCallback3 interface to receive notification that ranges of a file have completed downloading.
old-location: bits\ibackgroundcopycallback3.htm
tech.root: Bits
ms.assetid: 74712770-BB14-4B8A-8DA4-096CEB58D820
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBackgroundCopyCallback3, IBackgroundCopyCallback3 interface [BITS], IBackgroundCopyCallback3 interface [BITS],described, bits.ibackgroundcopycallback3, bits10_1/IBackgroundCopyCallback3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bits10_1.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyCallback3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyCallback3 interface


## -description


Clients implement the <b>IBackgroundCopyCallback3</b> interface to receive notification that ranges of a file have completed downloading.

Instead of polling for the download status of a file, clients use this interface.
To receive notifications, call the <a href="https://msdn.microsoft.com/en-us/library/Aa363045(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyInterface</a> method to specify the interface pointer to your <a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> implementation. To specify which notifications you want to receive, call the <a href="https://msdn.microsoft.com/en-us/library/Aa363044(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyFlags</a> method.
You must implement all methods of this interface and the <a href="https://msdn.microsoft.com/en-us/library/Aa362870(v=VS.85).aspx">IBackgroundCopyCallback2</a> and <b>IBackgroundCopyCallback</b> interface. For example, if you do not register for the file transferred callback, your <a href="https://msdn.microsoft.com/en-us/library/Aa362871(v=VS.85).aspx">FileTransferred</a> method must still return <b>S_OK</b>. If you do not want to receive the file ranges   transferred callback, you can simply implement the <b>IBackgroundCopyCallback</b> or <b>IBackgroundCopyCallback2</b> instead.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyCallback3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa362870(v=VS.85).aspx">IBackgroundCopyCallback2</a>. <b>IBackgroundCopyCallback3</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyCallback3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt492761(v=VS.85).aspx">FileRangesTransferred</a>
</td>
<td align="left" width="63%">
BITS calls your implementation of the <a href="https://msdn.microsoft.com/en-us/library/Mt492761(v=VS.85).aspx">FileRangesTransferred</a> method when one or more file ranges have been downloaded.  File ranges are added to the job using the <a href="https://msdn.microsoft.com/en-us/library/Mt492766(v=VS.85).aspx">IBackgroundCopyFile6::RequestFileRanges</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362867(v=VS.85).aspx">IBackgroundCopyCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362870(v=VS.85).aspx">IBackgroundCopyCallback2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363044(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyFlags</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363045(v=VS.85).aspx">IBackgroundCopyJob::SetNotifyInterface</a>
 

 

