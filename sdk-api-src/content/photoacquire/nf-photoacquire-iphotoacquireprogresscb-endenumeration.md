---
UID: NF:photoacquire.IPhotoAcquireProgressCB.EndEnumeration
title: IPhotoAcquireProgressCB::EndEnumeration method
author: windows-driver-content
description: The EndEnumeration method provides extended functionality when enumeration of files from the image source is complete. The application provides the implementation of the EndEnumeration method.
old-location: picacq\iphotoacquireprogresscb_endenumeration.htm
old-project: acquisition
ms.assetid: dac16ca2-bd80-4771-9e81-09d07958a4bb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EndEnumeration method [Picture Acquisition], EndEnumeration method [Picture Acquisition], IPhotoAcquireProgressCB interface, EndEnumeration,IPhotoAcquireProgressCB.EndEnumeration, IPhotoAcquireProgressCB, IPhotoAcquireProgressCB interface [Picture Acquisition], EndEnumeration method, IPhotoAcquireProgressCB::EndEnumeration, IPhotoAcquireProgressCBEndEnumeration, photoacquire/IPhotoAcquireProgressCB::EndEnumeration, picacq.iphotoacquireprogresscb_endenumeration
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IPhotoAcquireProgressCB.EndEnumeration
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPhotoAcquireProgressCB::EndEnumeration method


## -description



The <code>EndEnumeration</code> method provides extended functionality when enumeration of files from the image source is complete. The application provides the implementation of the <code>EndEnumeration</code> method.




## -parameters




### -param hr [in]

Specifies the result of the enumeration operation.


## -returns



The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values. Any failing HRESULT other than E_NOTIMPL is fatal and will cause the transfer to abort.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not yet implemented

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>
 

 

