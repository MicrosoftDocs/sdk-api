---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.GetCurrentOperationMode
title: IDMOVideoOutputOptimizations::GetCurrentOperationMode
author: windows-sdk-content
description: The GetCurrentOperationMode method retrieves the optimization features in effect.
old-location: dshow\idmovideooutputoptimizations_getcurrentoperationmode.htm
old-project: DirectShow
ms.assetid: ddfc65ea-e336-40b8-a901-53ebc3ee7d86
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetCurrentOperationMode, GetCurrentOperationMode method [DirectShow], GetCurrentOperationMode method [DirectShow],IDMOVideoOutputOptimizations interface, IDMOVideoOutputOptimizations interface [DirectShow],GetCurrentOperationMode method, IDMOVideoOutputOptimizations.GetCurrentOperationMode, IDMOVideoOutputOptimizations::GetCurrentOperationMode, IDMOVideoOutputOptimizationsGetCurrentOperationMode, dshow.idmovideooutputoptimizations_getcurrentoperationmode, mediaobj/IDMOVideoOutputOptimizations::GetCurrentOperationMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations.GetCurrentOperationMode
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOVideoOutputOptimizations::GetCurrentOperationMode


## -description



The <code>GetCurrentOperationMode</code> method retrieves the optimization features in effect.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pdwEnabledFeatures

Pointer to a variable that receives the current features. The returned value is a bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/fafacdd8-d918-491a-a7e5-7b59128f574f">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1e87d0e1-68be-4f86-aae2-cff3edfa573b">IDMOVideoOutputOptimizations Interface</a>
 

 

