---
UID: NF:mfidl.MFCreateSimpleTypeHandler
title: MFCreateSimpleTypeHandler function
author: windows-sdk-content
description: Creates a media-type handler that supports a single media type at a time.
old-location: mf\mfcreatesimpletypehandler.htm
old-project: medfound
ms.assetid: 441bd03d-b314-4f26-ad67-e6997e5edc9d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 441bd03d-b314-4f26-ad67-e6997e5edc9d, MFCreateSimpleTypeHandler, MFCreateSimpleTypeHandler function [Media Foundation], mf.mfcreatesimpletypehandler, mfidl/MFCreateSimpleTypeHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateSimpleTypeHandler
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateSimpleTypeHandler function


## -description



Creates a media-type handler that supports a single media type at a time.




## -parameters




### -param ppHandler [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a> interface of the media-type handler. The caller must release the interface.


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
</table>
 




## -remarks



The media-type handler created by this function supports one media type at a time. Set the media type by calling <a href="https://msdn.microsoft.com/77ff397e-4fa8-4849-98b8-6bdd035c0e89">IMFMediaTypeHandler::SetCurrentMediaType</a>. After the type is set, <a href="https://msdn.microsoft.com/ea52defa-8b78-4f40-97ae-ed6a5ee4849e">IMFMediaTypeHandler::IsMediaTypeSupported</a> always checks against that type.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

