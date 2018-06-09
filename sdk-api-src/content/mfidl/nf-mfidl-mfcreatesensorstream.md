---
UID: NF:mfidl.MFCreateSensorStream
title: MFCreateSensorStream function
author: windows-sdk-content
description: Creates an instance of the IMFSensorStream interface.
old-location: mf\mfcreatesensorstream.htm
old-project: medfound
ms.assetid: 3C260634-E722-4F1D-800C-FB32308CF605
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateSensorStream, MFCreateSensorStream function [Media Foundation], mf.mfcreatesensorstream, mfidl/MFCreateSensorStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCreateSensorStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateSensorStream function


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/9A5F6E25-796A-4798-8E4A-ABB9EB6A3B84">IMFSensorStream</a> interface.


## -parameters




### -param StreamId

The identifier for the created stream. This is the same as setting the <a href="https://msdn.microsoft.com/03C48CBA-FAD0-4127-89E5-3F1874BF32DB">MF_DEVICESTREAM_STREAM_ID</a> attribute. This value is used if <i>pAttributes</i> is null.


### -param pAttributes [in, optional]

The attribute store for the created stream.


### -param pMediaTypeCollection [in]

The collection of <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> objects specifying the media types supported by the stream.


### -param ppStream [out]

The created stream interface.


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied <a href="https://msdn.microsoft.com/7CED3EF6-E844-4B3A-8181-CA44FC4675EC">IMFSensorGroup</a> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <b>LPCWSTR</b> is null.

</td>
</tr>
</table>
 



