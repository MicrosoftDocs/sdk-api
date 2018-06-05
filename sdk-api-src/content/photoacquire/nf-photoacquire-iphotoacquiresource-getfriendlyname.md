---
UID: NF:photoacquire.IPhotoAcquireSource.GetFriendlyName
title: IPhotoAcquireSource::GetFriendlyName
author: windows-sdk-content
description: The GetFriendlyName method retrieves the name of the device, formatted for display.
old-location: picacq\iphotoacquiresource_getfriendlyname.htm
old-project: acquisition
ms.assetid: e6e1c5d7-b9d8-479a-a8e5-53124b55369d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: GetFriendlyName, GetFriendlyName method [Picture Acquisition], GetFriendlyName method [Picture Acquisition],IPhotoAcquireSource interface, IPhotoAcquireSource interface [Picture Acquisition],GetFriendlyName method, IPhotoAcquireSource.GetFriendlyName, IPhotoAcquireSource::GetFriendlyName, IPhotoAcquireSourceGetFriendlyName, photoacquire/IPhotoAcquireSource::GetFriendlyName, picacq.iphotoacquiresource_getfriendlyname
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoAcquireSource.GetFriendlyName
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPhotoAcquireSource::GetFriendlyName


## -description



The <code>GetFriendlyName</code> method retrieves the name of the device, formatted for display.




## -parameters




### -param pbstrFriendlyName [out]

Pointer to a string containing the friendly name.


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
A null value was passed where non-null is expected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

