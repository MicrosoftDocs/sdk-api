---
UID: NF:photoacquire.IPhotoAcquireSource.InitializeItemList
title: IPhotoAcquireSource::InitializeItemList (photoacquire.h)
author: windows-sdk-content
description: The InitializeItemList method enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.
old-location: picacq\iphotoacquiresource_initializeitemlist.htm
tech.root: acquisition
ms.assetid: 1e0ebbc7-888d-4044-8257-47c1719cf7fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireSource interface [Picture Acquisition],InitializeItemList method, IPhotoAcquireSource.InitializeItemList, IPhotoAcquireSource::InitializeItemList, IPhotoAcquireSourceInitializeItemList, InitializeItemList, InitializeItemList method [Picture Acquisition], InitializeItemList method [Picture Acquisition],IPhotoAcquireSource interface, photoacquire/IPhotoAcquireSource::InitializeItemList, picacq.iphotoacquiresource_initializeitemlist
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
 - IPhotoAcquireSource.InitializeItemList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSource::InitializeItemList


## -description



The <code>InitializeItemList</code> method enumerates transferable items on the device and passes each item to the optional progress callback, if it is supplied.




## -parameters




### -param fForceEnumeration [in]

Flag that, if set to <b>TRUE</b>, indicates that enumeration will be repeated even if the item list has already been initialized. If set to <b>FALSE</b>, this flag indicates that repeated calls to <code>InitializeItemList</code> after the item list has already been initialized will not enumerate items again.


### -param pPhotoAcquireProgressCB [in]

Optional. Pointer to an <a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB</a> object.


### -param pnItemCount [out]

Returns the number of items found.


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
Non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>
 




## -remarks



If <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a> is called without first calling <code>InitializeItemList</code>, initialization of the item list is done implicitly.

The first time the item list is initialized—either implicitly through <a href="https://msdn.microsoft.com/1000511f-40a6-4d5e-a55f-97e25f6c1e11">IPhotoAcquire::Acquire</a> or explicitly by calling <code>InitializeItemList</code>—each item is enumerated. During enumeration, if an <a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB</a> object is passed to <code>InitializeItemList</code>, its implementation of <a href="https://msdn.microsoft.com/ef42722d-ca39-4d22-8de1-6b3926669abf">StartEnumeration</a>, <a href="https://msdn.microsoft.com/b80fb2f2-57b7-4333-891e-32eba0347a17">FoundItem</a>, and <a href="https://msdn.microsoft.com/dac16ca2-bd80-4771-9e81-09d07958a4bb">EndEnumeration</a> may be used to apply further filtering or control to the list of items to be transferred.




## -see-also




<a href="https://msdn.microsoft.com/94f41290-bbc4-4a2f-9787-831004bde3c7">IPhotoAcquire Interface</a>



<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>



<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

