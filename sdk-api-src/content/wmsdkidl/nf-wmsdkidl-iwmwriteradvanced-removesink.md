---
UID: NF:wmsdkidl.IWMWriterAdvanced.RemoveSink
title: IWMWriterAdvanced::RemoveSink method
author: windows-driver-content
description: The RemoveSink method removes a writer sink object.
old-location: wmformat\iwmwriteradvanced_removesink.htm
old-project: wmformat
ms.assetid: e2fc7f82-981a-4f69-b99d-71514ed2c6ae
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWMWriterAdvanced, IWMWriterAdvanced interface [windows Media Format], RemoveSink method, IWMWriterAdvanced::RemoveSink, IWMWriterAdvancedRemoveSink, RemoveSink method [windows Media Format], RemoveSink method [windows Media Format], IWMWriterAdvanced interface, RemoveSink,IWMWriterAdvanced.RemoveSink, wmformat.iwmwriteradvanced_removesink, wmsdkidl/IWMWriterAdvanced::RemoveSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMWriterAdvanced.RemoveSink
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced::RemoveSink method


## -description



The <b>RemoveSink</b> method removes a writer sink object.




## -parameters




### -param pSink [in]

Pointer to the <a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a> interface of the sink object to remove, or <b>NULL</b> to remove all sinks.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not remove the specified sink.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer is not in a configurable state.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/65763ac3-fba0-4de6-9c2e-4e241bbe5f13">IWMWriterAdvanced::AddSink</a>



<a href="https://msdn.microsoft.com/6775eb89-a3af-42d2-b1e3-197abb1fce61">IWMWriterAdvanced::GetSink</a>
 

 

