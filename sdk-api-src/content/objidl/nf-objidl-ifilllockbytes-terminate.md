---
UID: NF:objidl.IFillLockBytes.Terminate
title: IFillLockBytes::Terminate (objidl.h)
description: The Terminate method informs the byte array that the download has been terminated, either successfully or unsuccessfully.
helpviewer_keywords: ["IFillLockBytes interface [Structured Storage]","Terminate method","IFillLockBytes.Terminate","IFillLockBytes::Terminate","Terminate","Terminate method [Structured Storage]","Terminate method [Structured Storage]","IFillLockBytes interface","_stg_ifilllockbytes_terminate","objidl/IFillLockBytes::Terminate","stg.ifilllockbytes_terminate"]
old-location: stg\ifilllockbytes_terminate.htm
tech.root: Stg
ms.assetid: 21ea78c7-51f1-4418-915c-79db47c25715
ms.date: 12/05/2018
ms.keywords: IFillLockBytes interface [Structured Storage],Terminate method, IFillLockBytes.Terminate, IFillLockBytes::Terminate, Terminate, Terminate method [Structured Storage], Terminate method [Structured Storage],IFillLockBytes interface, _stg_ifilllockbytes_terminate, objidl/IFillLockBytes::Terminate, stg.ifilllockbytes_terminate
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
 - IFillLockBytes::Terminate
 - objidl/IFillLockBytes::Terminate
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
 - IFillLockBytes.Terminate
---

# IFillLockBytes::Terminate


## -description

The <b>Terminate</b> method informs the byte array that the download has been terminated, either successfully or unsuccessfully.

## -parameters

### -param bCanceled [in]

Download is complete. If <b>TRUE</b>, the download was terminated unsuccessfully. If <b>FALSE</b>, the download terminated successfully.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL.

## -remarks

After this method has been called, the byte array will no longer return E_PENDING.

