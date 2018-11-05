---
UID: NF:wmcontainer.MFCreateASFMediaSink
title: MFCreateASFMediaSink function
author: windows-sdk-content
description: Creates the ASF media sink.
old-location: mf\mfcreateasfmediasink.htm
tech.root: medfound
ms.assetid: d800ac91-f6cc-4f57-9080-4bbafb42d7ed
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MFCreateASFMediaSink, MFCreateASFMediaSink function [Media Foundation], d800ac91-f6cc-4f57-9080-4bbafb42d7ed, mf.mfcreateasfmediasink, wmcontainer/MFCreateASFMediaSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmcontainer.h
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFMediaSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateASFMediaSink function


## -description



Creates the ASF media sink.




## -parameters




### -param pIByteStream

Pointer to a byte stream that will be used to write the ASF stream.


### -param ppIMediaSink

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.


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
 




## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>



<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

