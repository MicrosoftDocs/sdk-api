---
UID: NN:windowsstoragecom.IUnbufferedFileHandleOplockCallback
title: IUnbufferedFileHandleOplockCallback
author: windows-sdk-content
description: Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle method is broken.
old-location: winrt\iunbufferedfilehandleoplockcallback.htm
old-project: WinRT
ms.assetid: 7418EDE0-D9E1-4D8C-84B0-CAE9BDF053E3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUnbufferedFileHandleOplockCallback, IUnbufferedFileHandleOplockCallback interface [Windows Runtime], IUnbufferedFileHandleOplockCallback interface [Windows Runtime],described, windowsstoragecom/IUnbufferedFileHandleOplockCallback, winrt.iunbufferedfilehandleoplockcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windowsstoragecom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.storage.dll
api_name:
 - IUnbufferedFileHandleOplockCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.storage.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IUnbufferedFileHandleOplockCallback interface


## -description


Defines a callback method that you want to run when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUnbufferedFileHandleOplockCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUnbufferedFileHandleOplockCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUnbufferedFileHandleOplockCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F5B6B4F6-61F2-4C5A-9E63-E9DC876FEB60">OnBrokenCallback</a>
</td>
<td align="left" width="63%">
Runs when the opportunistic lock for a handle that you get by calling the <a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a> method is broken.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/D001CD90-A621-403C-B9BD-BE79471AF18F">IUnbufferedFileHandleProvider::OpenUnbufferedFileHandle</a>
 

 

