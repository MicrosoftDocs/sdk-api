---
UID: NN:objidl.ILockBytes
title: ILockBytes (objidl.h)
description: The ILockBytes interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database.
old-location: stg\ilockbytes.htm
tech.root: Stg
ms.assetid: bb2c5d0d-8dc8-4844-9a20-ef8e4def5731
ms.date: 12/05/2018
ms.keywords: ILockBytes, ILockBytes interface [Structured Storage], ILockBytes interface [Structured Storage],described, _stg_ilockbytes, objidl/ILockBytes, stg.ilockbytes
ms.topic: interface
f1_keywords:
- objidl/ILockBytes
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- ILockBytes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILockBytes interface


## -description


The 
<b>ILockBytes</b> interface is implemented on a byte array object that is backed by some physical storage, such as a disk file, global memory, or a database. It is used by a COM compound file storage object to give its root storage access to the physical device, while isolating the root storage from the details of accessing the physical storage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILockBytes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILockBytes</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-flush">Flush</a>
</td>
<td align="left" width="63%">
Ensures that any internal buffers maintained by the byte array object are written out to the backing storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-lockregion">LockRegion</a>
</td>
<td align="left" width="63%">
Restricts access to a specified range of bytes in the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ReadAt</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes starting at a specified offset from the beginning of the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Changes the size of the byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">Stat</a>
</td>
<td align="left" width="63%">
Retrieves a 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure for this byte array object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-unlockregion">UnlockRegion</a>
</td>
<td align="left" width="63%">
Removes the access restriction on a range of bytes previously restricted with 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-lockregion">ILockBytes::LockRegion</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-writeat">WriteAt</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes to a specified location in the byte array.

</td>
</tr>
</table> 

