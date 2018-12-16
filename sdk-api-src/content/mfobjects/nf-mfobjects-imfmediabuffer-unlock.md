---
UID: NF:mfobjects.IMFMediaBuffer.Unlock
title: IMFMediaBuffer::Unlock
author: windows-sdk-content
description: Unlocks a buffer that was previously locked. Call this method once for every call to IMFMediaBuffer::Lock.
old-location: mf\imfmediabuffer_unlock.htm
tech.root: medfound
ms.assetid: 3ca53321-5533-45f0-b415-6a16f780ec54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 3ca53321-5533-45f0-b415-6a16f780ec54, IMFMediaBuffer interface [Media Foundation],Unlock method, IMFMediaBuffer.Unlock, IMFMediaBuffer::Unlock, Unlock, Unlock method [Media Foundation], Unlock method [Media Foundation],IMFMediaBuffer interface, mf.imfmediabuffer_unlock, mfobjects/IMFMediaBuffer::Unlock
ms.topic: method
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
 - IMFMediaBuffer.Unlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaBuffer::Unlock


## -description



Unlocks a buffer that was previously locked. Call this method once for every call to <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
For Direct3D surface buffers, an error occurred when unlocking the surface.

</td>
</tr>
</table>
 




## -remarks



It is an error to call <b>Unlock</b> if you did not call <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">Lock</a> previously.

After calling this method, do not use the pointer returned by the <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">Lock</a> method. It is no longer guaranteed to be valid.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>
 

 

