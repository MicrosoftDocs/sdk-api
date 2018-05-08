---
UID: NF:photoacquire.IPhotoAcquire.Acquire
title: IPhotoAcquire::Acquire
author: windows-driver-content
description: The Acquire method acquires photos from a device.
old-location: picacq\iphotoacquire_acquire.htm
old-project: acquisition
ms.assetid: 1000511f-40a6-4d5e-a55f-97e25f6c1e11
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Acquire, Acquire method [Picture Acquisition], Acquire method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],Acquire method, IPhotoAcquire.Acquire, IPhotoAcquire::Acquire, IPhotoAcquireAcquire, photoacquire/IPhotoAcquire::Acquire, picacq.iphotoacquire_acquire
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
-	IPhotoAcquire.Acquire
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPhotoAcquire::Acquire


## -description



The <code>Acquire</code> method acquires photos from a device.




## -parameters




### -param pPhotoAcquireSource [in]

Pointer to an <a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource</a> object representing the device from which to acquire photos. Initialize this object by calling <a href="https://msdn.microsoft.com/03dc14d4-03e8-4281-ae70-c9f2c5646694">CreatePhotoSource</a>.


### -param fShowProgress [in]

Flag that, when set to <b>TRUE</b>, indicates that a progress dialog will be shown.


### -param hWndParent [in]

Handle to a parent window.


### -param pszApplicationName [in]

Pointer to a null-terminated string containing the application name.


### -param pPhotoAcquireProgressCB [in]

Pointer to an optional <a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB</a> object.


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



To initialize the <i>pPhotoAcquireSource</i> parameter passed to <code>Acquire</code>, <a href="https://msdn.microsoft.com/03dc14d4-03e8-4281-ae70-c9f2c5646694">CreatePhotoSource</a> should be called prior to calling <code>Acquire</code>.

<i>pPhotoAcquireProgressCB</i> provides callback methods that allow you to apply further filtering or control as items are acquired.

To verify that there are items in the device before acquisition, or to selectively acquire items from the device, call <a href="https://msdn.microsoft.com/1e0ebbc7-888d-4044-8257-47c1719cf7fc">IPhotoAcquireSource::InitializeItemList</a> to enumerate the items before calling <code>Acquire</code>.




## -see-also




<a href="https://msdn.microsoft.com/94f41290-bbc4-4a2f-9787-831004bde3c7">IPhotoAcquire Interface</a>



<a href="https://msdn.microsoft.com/c4fcc470-1b05-4d33-8581-80c6e7488e04">IPhotoAcquireProgressCB Interface</a>



<a href="https://msdn.microsoft.com/6671d550-8c12-40e3-bf6f-33203e69cff0">IPhotoAcquireSource Interface</a>
 

 

