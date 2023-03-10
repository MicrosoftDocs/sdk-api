---
UID: NF:objidl.ILockBytes.SetSize
title: ILockBytes::SetSize (objidl.h)
description: The SetSize method changes the size of the byte array.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","SetSize method","ILockBytes.SetSize","ILockBytes::SetSize","SetSize","SetSize method [Structured Storage]","SetSize method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_setsize","objidl/ILockBytes::SetSize","stg.ilockbytes_setsize"]
old-location: stg\ilockbytes_setsize.htm
tech.root: Stg
ms.assetid: 13b3237b-d113-4505-b397-b06916368fef
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],SetSize method, ILockBytes.SetSize, ILockBytes::SetSize, SetSize, SetSize method [Structured Storage], SetSize method [Structured Storage],ILockBytes interface, _stg_ilockbytes_setsize, objidl/ILockBytes::SetSize, stg.ilockbytes_setsize
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
 - ILockBytes::SetSize
 - objidl/ILockBytes::SetSize
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
 - ILockBytes.SetSize
---

# ILockBytes::SetSize


## -description

The <b>SetSize</b> method changes the size of the byte array.

## -parameters

### -param cb [in]

Specifies the new size of the byte array as a number of bytes.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The size of the byte array was successfully changed.|
|STG_E_ACCESSDENIED | The caller does not have permission to access the byte array.|
|STG_E_MEDIUMFULL | The byte array size is not changed because there is no space left on the storage device.|

## -remarks

<b>ILockBytes::SetSize</b> changes the size of the byte array. If the <i>cb</i> parameter is larger than the current byte array, the byte array is extended to the indicated size by filling the intervening space with bytes of undefined value, as does 
<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-writeat">ILockBytes::WriteAt</a>, if the seek pointer is past the current end-of-stream.

If the <i>cb</i> parameter is smaller than the current byte array, the byte array is truncated to the indicated size.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Callers cannot rely on STG_E_MEDIUMFULL being returned at the appropriate time because of cache buffering in the operating system or network. However, callers must be able to deal with this return code because some 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> implementations might support it.

## -see-also

<a href="/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-writeat">ILockBytes::WriteAt</a>