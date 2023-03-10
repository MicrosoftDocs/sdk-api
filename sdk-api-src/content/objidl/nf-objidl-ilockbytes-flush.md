---
UID: NF:objidl.ILockBytes.Flush
title: ILockBytes::Flush (objidl.h)
description: The Flush method ensures that any internal buffers maintained by the ILockBytes implementation are written out to the underlying physical storage.
helpviewer_keywords: ["Flush","Flush method [Structured Storage]","Flush method [Structured Storage]","ILockBytes interface","ILockBytes interface [Structured Storage]","Flush method","ILockBytes.Flush","ILockBytes::Flush","_stg_ilockbytes_flush","objidl/ILockBytes::Flush","stg.ilockbytes_flush"]
old-location: stg\ilockbytes_flush.htm
tech.root: Stg
ms.assetid: 9396c44f-ad76-49f4-9796-d29570466a27
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [Structured Storage], Flush method [Structured Storage],ILockBytes interface, ILockBytes interface [Structured Storage],Flush method, ILockBytes.Flush, ILockBytes::Flush, _stg_ilockbytes_flush, objidl/ILockBytes::Flush, stg.ilockbytes_flush
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILockBytes::Flush
 - objidl/ILockBytes::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes.Flush
---

# ILockBytes::Flush


## -description

The 
<b>Flush</b> method ensures that any internal buffers maintained by the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> implementation are written out to the underlying physical storage.



## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The flush operation was successful.|
|STG_E_ACCESSDENIED | The caller does not have permission to access the byte array.|
|STG_E_MEDIUMFULL | The flush operation is not completed because there is no space left on the storage device.|
|E_FAIL | General failure writing data.|
|STG_E_TOOMANYFILESOPEN | Under certain circumstances, the **Flush** method executes a download-and-closeto flush, which can lead to a return value of STG_E_TOOMANYFILESOPEN if no file handles are available.|
|STG_E_INVALIDHANDLE | An underlying file has been prematurely closed, or the correct floppy disk has been replaced by an invalid one.|

## -remarks

<b>ILockBytes::Flush</b> flushes internal buffers to the underlying storage device.

The COM-provided implementation of compound files calls this method during a transacted commit operation to provide a two-phase commit process that protects against loss of data.

## -see-also

<a href="/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>
