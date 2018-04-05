---
UID: NF:mfapi.MFCreateMemoryBuffer
title: MFCreateMemoryBuffer function
author: windows-driver-content
description: Allocates system memory and creates a media buffer to manage it.
old-location: mf\mfcreatememorybuffer.htm
old-project: medfound
ms.assetid: 1f79d057-7ef7-4662-9f82-ceadc23276f0
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 1f79d057-7ef7-4662-9f82-ceadc23276f0, MFCreateMemoryBuffer, MFCreateMemoryBuffer function [Media Foundation], mf.mfcreatememorybuffer, mfapi/MFCreateMemoryBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateMemoryBuffer
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMemoryBuffer function


## -description



Allocates system memory and creates a media buffer to manage it.




## -parameters




### -param cbMaxLength

Size of the buffer, in bytes.


### -param ppBuffer

Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of the media buffer. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The function allocates a buffer with a 1-byte memory alignment. To allocate a buffer that is aligned to a larger memory boundary, call <a href="https://msdn.microsoft.com/cccc0dea-3f1e-41e4-97f4-de7760ceccb0">MFCreateAlignedMemoryBuffer</a>.

When the media buffer object is destroyed, it releases the allocated memory.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

