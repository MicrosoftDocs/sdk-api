---
UID: NF:callobj.ICallFrame.Unmarshal
title: ICallFrame::Unmarshal
author: windows-sdk-content
description: Unmarshals a packet of data containing the previously marshaled [out] parameters of a call into this already existing activation record.
old-location: com\icallframe_unmarshal.htm
tech.root: com
ms.assetid: 9f604366-0e1f-4e04-9843-13c77ea573ab
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ICallFrame interface [COM],Unmarshal method, ICallFrame.Unmarshal, ICallFrame::Unmarshal, Unmarshal, Unmarshal method [COM], Unmarshal method [COM],ICallFrame interface, _com_icallframe_unmarshal, callobj/ICallFrame::Unmarshal, com.icallframe_unmarshal
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.Unmarshal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFrame::Unmarshal


## -description


Unmarshals a packet of data containing the previously marshaled [out] parameters of a call into this already existing activation record.


## -parameters




### -param pBuffer [in]

A pointer to the buffer containing the marshaled [out] values.


### -param cbBuffer [in]

The size of the buffer, in bytes.


### -param dataRep [in]

The NDR data representation with which the data was marshaled. For more information, see <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>.


### -param pcontext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how unmarshalling is carried out.


### -param pcbUnmarshalled [out]

Receives the number of bytes that were successfully unmarshaled. This parameter is returned even in error situations. This parameter is optional.


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



When unmarshalling, the [in] versions of [in, out] parameters are freed and interface pointers are released and replaced with there [out] versions. All the [in, out] and [out] parameters will always be set to reasonable [in], [in, out] values, [out] values successfully unmarshaled from the returned data, or a value explicitly initialized to <b>NULL</b>. On failure return, the caller will typically want to call <a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">ICallFrame::Free</a> in order to clean up the values that are not <b>NULL</b>.






## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

