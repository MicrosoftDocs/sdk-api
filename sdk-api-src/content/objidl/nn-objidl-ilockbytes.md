---
UID: NN:objidl.ILockBytes
title: ILockBytes
author: windows-sdk-content
description: The ILockBytes interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database.
old-location: stg\ilockbytes.htm
old-project: Stg
ms.assetid: bb2c5d0d-8dc8-4844-9a20-ef8e4def5731
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ILockBytes, ILockBytes interface [Structured Storage], ILockBytes interface [Structured Storage],described, _stg_ilockbytes, objidl/ILockBytes, stg.ilockbytes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# ILockBytes interface


## -description


The 
<b>ILockBytes</b> interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database. It is used by a COM compound file storage object to give its root storage access to the physical device, while isolating the root storage from the details of accessing the physical storage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILockBytes</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILockBytes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILockBytes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9396c44f-ad76-49f4-9796-d29570466a27">Flush</a>
</td>
<td align="left" width="63%">
Ensures that any internal buffers maintained by the byte array object are written out to the backing storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">LockRegion</a>
</td>
<td align="left" width="63%">
Restricts access to a specified range of bytes in the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ReadAt</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes starting at a specified offset from the beginning of the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13b3237b-d113-4505-b397-b06916368fef">SetSize</a>
</td>
<td align="left" width="63%">
Changes the size of the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">Stat</a>
</td>
<td align="left" width="63%">
Retrieves a 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure for this byte array object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/036ba242-8630-4013-860d-dd37919253be">UnlockRegion</a>
</td>
<td align="left" width="63%">
Removes the access restriction on a range of bytes previously restricted with 
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a27af4e1-293d-438a-8068-87275a51fd48">WriteAt</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes to a specified location in the byte array.

</td>
</tr>
</table> 

