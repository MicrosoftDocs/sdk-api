---
UID: NF:photoacquire.IPhotoAcquire.EnumResults
title: IPhotoAcquire::EnumResults
author: windows-sdk-content
description: The EnumResults method retrieves an enumeration containing the paths of all files successfully transferred during the most recent call to Acquire.
old-location: picacq\iphotoacquire_enumresults.htm
old-project: acquisition
ms.assetid: 2f3bd36c-3daf-4738-8240-ce622d988861
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EnumResults, EnumResults method [Picture Acquisition], EnumResults method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],EnumResults method, IPhotoAcquire.EnumResults, IPhotoAcquire::EnumResults, IPhotoAcquireEnumResults, photoacquire/IPhotoAcquire::EnumResults, picacq.iphotoacquire_enumresults
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: photoacquire.h
req.include-header: 
req.redist: 
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquire.EnumResults
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquire::EnumResults


## -description



The <code>EnumResults</code> method retrieves an enumeration containing the paths of all files successfully transferred during the most recent call to <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">Acquire</a>.




## -parameters




### -param ppEnumFilePaths [out]

Returns an enumeration containing the paths to all the transferred files.


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



If the file transfer is aborted before any files are transferred, <i>ppEnumFilePaths</i> will be set to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/94f41290-bbc4-4a2f-9787-831004bde3c7">IPhotoAcquire Interface</a>



<a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a>
 

 

