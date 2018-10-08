---
UID: NF:mfobjects.IMFAttributes.UnlockStore
title: IMFAttributes::UnlockStore
author: windows-sdk-content
description: Unlocks the attribute store after a call to the IMFAttributes::LockStore method. While the object is unlocked, multiple threads can access the object's attributes.
old-location: mf\imfattributes_unlockstore.htm
tech.root: medfound
ms.assetid: 65e35864-868a-4ae9-86ed-772a2b2daeb6
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 65e35864-868a-4ae9-86ed-772a2b2daeb6, IMFAttributes interface [Media Foundation],UnlockStore method, IMFAttributes.UnlockStore, IMFAttributes::UnlockStore, UnlockStore, UnlockStore method [Media Foundation], UnlockStore method [Media Foundation],IMFAttributes interface, mf.imfattributes_unlockstore, mfobjects/IMFAttributes::UnlockStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.UnlockStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAttributes::UnlockStore


## -description



Unlocks the attribute store after a call to the <a href="https://msdn.microsoft.com/6ec7aed3-7dbc-4aa4-92d5-646aee757db7">IMFAttributes::LockStore</a> method. While the object is unlocked, multiple threads can access the object's attributes.




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



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>
 

 

