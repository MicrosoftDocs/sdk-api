---
UID: NF:objidl.ILayoutStorage.ReLayoutDocfileOnILockBytes
title: ILayoutStorage::ReLayoutDocfileOnILockBytes
author: windows-sdk-content
description: Is not implemented. If called, it returns STG_E_UNIMPLEMENTEDFUNCTION.
old-location: stg\ilayoutstorage_relayoutdocfileonilockbytes.htm
tech.root: stg
ms.assetid: 4d62ea35-d9cb-4ec6-ad71-7b32096953f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILayoutStorage interface [Structured Storage],ReLayoutDocfileOnILockBytes method, ILayoutStorage.ReLayoutDocfileOnILockBytes, ILayoutStorage::ReLayoutDocfileOnILockBytes, ReLayoutDocfileOnILockBytes, ReLayoutDocfileOnILockBytes method [Structured Storage], ReLayoutDocfileOnILockBytes method [Structured Storage],ILayoutStorage interface, objidl/ILayoutStorage::ReLayoutDocfileOnILockBytes, stg.ilayoutstorage_relayoutdocfileonilockbytes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ILayoutStorage.ReLayoutDocfileOnILockBytes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILayoutStorage::ReLayoutDocfileOnILockBytes


## -description


Not supported.

The <b>ReLayoutDocfileOnILockBytes</b> method is not implemented.   If called, it returns  <b>STG_E_UNIMPLEMENTEDFUNCTION</b>.


## -parameters




### -param pILockBytes [in]

A pointer to the <a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the underlying byte-array object where the compound file is to be rewritten.


## -returns



This method returns the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_UNIMPLEMENTEDFUNCTION</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
 




## -remarks



If implemented, it would rewrite the compound file in the byte-array object specified by the caller.  It would return <b>S_OK</b> for success or one of the <b>STG_E_*</b> error codes for failure.



