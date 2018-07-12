---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.QueryOperationModePreferences
title: IDMOVideoOutputOptimizations::QueryOperationModePreferences
author: windows-sdk-content
description: The QueryOperationModePreferences method retrieves the DMO's preferred optimization features.
old-location: dshow\idmovideooutputoptimizations_queryoperationmodepreferences.htm
old-project: DirectShow
ms.assetid: 55916330-8395-4952-a349-f1ab5a3a2d64
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDMOVideoOutputOptimizations interface [DirectShow],QueryOperationModePreferences method, IDMOVideoOutputOptimizations.QueryOperationModePreferences, IDMOVideoOutputOptimizations::QueryOperationModePreferences, IDMOVideoOutputOptimizationsQueryOperationModePreferences, QueryOperationModePreferences, QueryOperationModePreferences method [DirectShow], QueryOperationModePreferences method [DirectShow],IDMOVideoOutputOptimizations interface, dshow.idmovideooutputoptimizations_queryoperationmodepreferences, mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences
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
 - IDMOVideoOutputOptimizations.QueryOperationModePreferences
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDMOVideoOutputOptimizations::QueryOperationModePreferences


## -description



The <code>QueryOperationModePreferences</code> method retrieves the DMO's preferred optimization features.




## -parameters




### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pdwRequestedCapabilities

Pointer to a variable that receives the DMO's requested features. The returned value is a bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/fafacdd8-d918-491a-a7e5-7b59128f574f">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.


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
 

 

