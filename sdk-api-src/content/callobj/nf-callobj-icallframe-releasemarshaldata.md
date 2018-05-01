---
UID: NF:callobj.ICallFrame.ReleaseMarshalData
title: ICallFrame::ReleaseMarshalData method
author: windows-driver-content
description: Releases resources that are held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet, and calls the CoReleaseMarshalData function on each one.
old-location: com\icallframe_releasemarshaldata.htm
old-project: com
ms.assetid: c82107ad-68d1-4a46-ba78-37592d445c57
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: ICallFrame, ICallFrame interface [COM], ReleaseMarshalData method, ICallFrame::ReleaseMarshalData, ReleaseMarshalData method [COM], ReleaseMarshalData method [COM], ICallFrame interface, ReleaseMarshalData,ICallFrame.ReleaseMarshalData, _com_icallframe_releasemarshaldata, callobj/ICallFrame::ReleaseMarshalData, com.icallframe_releasemarshaldata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CALLFRAME_COPY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Callobj.h
api_name:
-	ICallFrame.ReleaseMarshalData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::ReleaseMarshalData method


## -description


Releases resources that are held by interface pointers residing in a packet of marshaled data. This method finds all interface pointers in the packet, and calls the <a href="https://msdn.microsoft.com/a642a20f-3a3c-46bc-b833-e424dab3a16d">CoReleaseMarshalData</a> function on each one.



## -parameters




### -param pBuffer [in]

A pointer to the buffer containing the marshaled [out] values.


### -param cbBuffer [in]

The size of the buffer, in bytes.


### -param ibFirstRelease [in]

The first byte in the buffer, which is to be released. A value of zero implies that the interface pointers in the whole buffer are to be released. The marshaled interface pointers are assumed to have been released by some other mechanism.


### -param dataRep [in]

The data representation with which the data was marshaled.


### -param pcontext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how un-marshalling is carried out.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>ReleaseMarshalData</b> method must be called exactly once to clean up the resources held in a marshaled buffer. However when the <a href="https://msdn.microsoft.com/42a482be-d4b8-4f2e-ae43-1d210cb44c7c">MSHLFLAGS</a> enumeration is set to MSHLFLAGS_NORMAL, this is done automatically during un-marshaling and so need not be carried out explicitly.

This method can function correctly on both marshaled [in] and [out] parameters.




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

