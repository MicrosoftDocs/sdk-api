---
UID: NF:mfapi.MFLockPlatform
title: MFLockPlatform function
author: windows-sdk-content
description: Blocks the MFShutdown function.
old-location: mf\mflockplatform.htm
old-project: medfound
ms.assetid: 040742dc-4ba3-4906-8257-65505b2924d5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 040742dc-4ba3-4906-8257-65505b2924d5, MFLockPlatform, MFLockPlatform function [Media Foundation], mf.mflockplatform, mfapi/MFLockPlatform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFLockPlatform
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFLockPlatform function


## -description



Blocks the <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function.




## -parameters






## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



This function prevents work queue threads from being shut down when <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> is called. Use this function to ensure that asynchronous operations complete gracefully before the platform shuts down.

This function holds a lock on the Media Foundation platform. To unlock the platform, call <a href="https://msdn.microsoft.com/d4ce5315-4bb2-4ca4-a9a0-20b638a43040">MFUnlockPlatform</a>. The application must call <b>MFUnlockPlatform</b> once for every call to <b>MFLockPlatform</b>.

The <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function blocks until the platform is unlocked, or until a fixed wait period has elapsed. (The wait period is a few seconds.) To avoid memory leaks, the application should unlock the platform before the wait period ends. For example, cancel any asynchronous operations that are waiting to complete and are holding a lock on the platform.

The default implementation of the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface automatically locks the Media Foundation platform when the result object is created. Releasing the interface unlocks the platform. Therefore, in most cases your application does not need to lock the platform directly. For more information, see <a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/1eb20c44-58cb-4e34-a108-1b3c27d54ff1">Media Foundation Platform APIs</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

