---
UID: NN:mfobjects.IMFAsyncResult
title: IMFAsyncResult (mfobjects.h)
author: windows-sdk-content
description: Provides information about the result of an asynchronous operation.
old-location: mf\imfasyncresult.htm
tech.root: medfound
ms.assetid: 8c95b1de-8974-445c-8070-41552ea83e53
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8c95b1de-8974-445c-8070-41552ea83e53, IMFAsyncResult, IMFAsyncResult interface [Media Foundation], IMFAsyncResult interface [Media Foundation],described, mf.imfasyncresult, mfobjects/IMFAsyncResult
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAsyncResult interface


## -description


Provides information about the result of an asynchronous operation.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAsyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFAsyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAsyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4b871ff-370d-4a37-9fe4-91d1805890eb">GetObject</a>
</td>
<td align="left" width="63%">
Returns an object associated with the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8ed8e71-6df7-4c94-b400-b4651a00db5b">GetState</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37ba820c-5253-48de-a960-c546e50e8672">GetStateNoAddRef</a>
</td>
<td align="left" width="63%">
Returns the state object specified by the caller in the asynchronous <b>Begin</b> method, without incrementing the object's reference count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad99f3dd-4885-42e8-8f4e-060d522dde7b">GetStatus</a>
</td>
<td align="left" width="63%">
Returns the status of the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79dec067-ba54-435b-8744-9a6f43dd416d">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the asynchronous operation.

</td>
</tr>
</table> 


## -remarks



Use this interface to complete an asynchronous operation. You get a pointer to this interface when your callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. To complete the operation, pass the <b>IMFAsyncResult</b> pointer to the <b>End...</b> method that corresponds to the <b>Begin...</b> method that starts the operation. For example, if the asynchronous method is named <b>BeginRead</b>, call the <b>EndRead</b> method. For more information, see <a href="https://msdn.microsoft.com/1d8688a5-d476-457d-a0ad-e4f106ac3484">Calling Asynchronous Methods</a>.

If you are implementing an asynchronous method, call <a href="https://msdn.microsoft.com/6ff773a9-961e-4a5e-ad37-46234022c575">MFCreateAsyncResult</a> to create an instance of this object. For more information, see <a href="https://msdn.microsoft.com/cd94280d-7267-4d35-8333-aa4a5bd81b73">Writing an Asynchronous Method</a>.

Any custom implementation of this interface must inherit the <a href="https://msdn.microsoft.com/fffa32d6-5e9f-42a1-9978-04f5726528bc">MFASYNCRESULT</a> structure.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ea778eaa-6460-4a93-bd6a-1857ea8b6230">Asynchronous Callback Methods</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

