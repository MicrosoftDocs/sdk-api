---
UID: NF:wmsdkidl.WMCreateWriterFileSink
title: WMCreateWriterFileSink function
author: windows-sdk-content
description: The WMCreateWriterFileSink function creates a writer file sink object.
old-location: wmformat\wmcreatewriterfilesink.htm
tech.root: wmformat
ms.assetid: aeeaf67c-119f-482b-b064-87739499abda
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WMCreateWriterFileSink, WMCreateWriterFileSink function [windows Media Format], wmformat.wmcreatewriterfilesink, wmsdkidl/WMCreateWriterFileSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateWriterFileSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WMCreateWriterFileSink
: 
---

# WMCreateWriterFileSink function


## -description



The <b>WMCreateWriterFileSink</b> function creates a writer file sink object.




## -parameters




### -param ppSink [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/af47b130-353e-411d-8432-09ecd20a70d2">IWMWriterFileSink</a> interface of the newly created writer file sink object.


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
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>



<a href="https://msdn.microsoft.com/93f44579-fb2d-498e-a271-5bc91d6f0321">Writer File Sink Object</a>
 

 

