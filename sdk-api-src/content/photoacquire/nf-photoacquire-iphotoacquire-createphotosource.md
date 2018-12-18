---
UID: NF:photoacquire.IPhotoAcquire.CreatePhotoSource
title: IPhotoAcquire::CreatePhotoSource
author: windows-sdk-content
description: The CreatePhotoSource method initializes an IPhotoAcquireSource object to pass to IPhotoAcquire::Acquire.
old-location: picacq\iphotoacquire_createphotosource.htm
tech.root: acquisition
ms.assetid: 03dc14d4-03e8-4281-ae70-c9f2c5646694
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreatePhotoSource, CreatePhotoSource method [Picture Acquisition], CreatePhotoSource method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],CreatePhotoSource method, IPhotoAcquire.CreatePhotoSource, IPhotoAcquire::CreatePhotoSource, IPhotoAcquireCreatePhotoSource, photoacquire/IPhotoAcquire::CreatePhotoSource, picacq.iphotoacquire_createphotosource
ms.topic: method
req.header: photoacquire.h
req.include-header: 
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquire.CreatePhotoSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquire::CreatePhotoSource


## -description



The <code>CreatePhotoSource</code> method initializes an <a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource</a> object to pass to <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a>.




## -parameters




### -param pszDevice [in]

Pointer to a null-terminated string containing the device name.


### -param ppPhotoAcquireSource [out]

Returns the initialized photo source to acquire photos from.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource</a> object created is used as the parameter for the <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">Acquire</a> method.

If an error occurs in <code>CreatePhotoSource</code>, <i>ppPhotoAcquireSource</i> is initialized to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/94f41290-bbc4-4a2f-9787-831004bde3c7">IPhotoAcquire Interface</a>



<a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a>
 

 

