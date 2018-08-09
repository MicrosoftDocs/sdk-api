---
UID: NF:sbe.IStreamBufferConfigure.SetBackingFileDuration
title: IStreamBufferConfigure::SetBackingFileDuration
author: windows-sdk-content
description: The SetBackingFileDuration method sets the duration of all backing files.
old-location: mstv\istreambufferconfigure_setbackingfileduration.htm
old-project: mstv
ms.assetid: 1825896e-0e3c-4b89-8e0e-59faa0f8000d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IStreamBufferConfigure interface [Microsoft TV Technologies],SetBackingFileDuration method, IStreamBufferConfigure.SetBackingFileDuration, IStreamBufferConfigure::SetBackingFileDuration, IStreamBufferConfigureSetBackingFileDuration, SetBackingFileDuration, SetBackingFileDuration method [Microsoft TV Technologies], SetBackingFileDuration method [Microsoft TV Technologies],IStreamBufferConfigure interface, mstv.istreambufferconfigure_setbackingfileduration, sbe/IStreamBufferConfigure::SetBackingFileDuration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure.SetBackingFileDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferConfigure::SetBackingFileDuration


## -description


The <b>SetBackingFileDuration</b> method sets the duration of all backing files.


## -parameters




### -param dwSeconds [in]

Specifies the file duration, in seconds. The minimum value is 15.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object was not initialized.

</td>
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
</table>
 




## -remarks



Before calling this method, call <a href="https://msdn.microsoft.com/f8d85180-2575-4525-9b8a-bec354e2cd4c">IStreamBufferInitialize::SetHKEY</a> to specify a registry key where the information will be stored.




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure Interface</a>
 

 

