---
UID: NF:mfapi.MFCreateLegacyMediaBufferOnMFMediaBuffer
title: MFCreateLegacyMediaBufferOnMFMediaBuffer function
author: windows-sdk-content
description: Converts a Media Foundation media buffer into a buffer that is compatible with DirectX Media Objects (DMOs).
old-location: mf\mfcreatelegacymediabufferonmfmediabuffer.htm
tech.root: medfound
ms.assetid: 35d749d8-2bca-4fe8-b145-175e178ae529
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 35d749d8-2bca-4fe8-b145-175e178ae529, MFCreateLegacyMediaBufferOnMFMediaBuffer, MFCreateLegacyMediaBufferOnMFMediaBuffer function [Media Foundation], mf.mfcreatelegacymediabufferonmfmediabuffer, mfapi/MFCreateLegacyMediaBufferOnMFMediaBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateLegacyMediaBufferOnMFMediaBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateLegacyMediaBufferOnMFMediaBuffer function


## -description



Converts a Media Foundation media buffer into a buffer that is compatible with DirectX Media Objects (DMOs).




## -parameters




### -param pSample

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the sample that contains the Media Foundation buffer. This parameter can be <b>NULL</b>.


### -param pMFMediaBuffer

Pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of the Media Foundation buffer.


### -param cbOffset

Offset in bytes from the start of the Media Foundation buffer. This offset defines where the DMO buffer starts. If this parameter is zero, the DMO buffer starts at the beginning of the Media Foundation buffer.


### -param ppMediaBuffer

Receives a pointer to the <b>IMediaBuffer</b> interface. This interface is documented in the DirectShow SDK documentation. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. The <i>pIMFMediaBuffer</i> parameter must not be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The DMO buffer created by this function also exposes the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface. If <i>pIMFSample</i> is <b>NULL</b>, all of the <b>IMFSample</b> methods return MF_E_NOT_INITIALIZED. Otherwise, they call through to the <i>pIMFSample</i> pointer.

If the Media Foundation buffer specified by <i>pIMFMediaBuffer</i> exposes the <a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a> interface, the DMO buffer also exposes <b>IMF2DBuffer</b>.




## -see-also




<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>



<a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>



<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

