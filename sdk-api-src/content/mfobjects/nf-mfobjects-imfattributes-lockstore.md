---
UID: NF:mfobjects.IMFAttributes.LockStore
title: IMFAttributes::LockStore
author: windows-driver-content
description: Locks the attribute store so that no other thread can access it.
old-location: mf\imfattributes_lockstore.htm
old-project: medfound
ms.assetid: 6ec7aed3-7dbc-4aa4-92d5-646aee757db7
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 6ec7aed3-7dbc-4aa4-92d5-646aee757db7, IMFAttributes interface [Media Foundation],LockStore method, IMFAttributes.LockStore, IMFAttributes::LockStore, LockStore, LockStore method [Media Foundation], LockStore method [Media Foundation],IMFAttributes interface, mf.imfattributes_lockstore, mfobjects/IMFAttributes::LockStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAttributes.LockStore
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::LockStore


## -description



Locks the attribute store so that no other thread can access it. If the attribute store is already locked by another thread, this method blocks until the other thread unlocks the object. After calling this method, call <a href="https://msdn.microsoft.com/65e35864-868a-4ae9-86ed-772a2b2daeb6">IMFAttributes::UnlockStore</a> to unlock the object.




## -parameters






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
</table>
 




## -remarks



This method can cause a deadlock if a thread that calls <b>LockStore</b> waits on a thread that calls any other <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> methods on the same object.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 

