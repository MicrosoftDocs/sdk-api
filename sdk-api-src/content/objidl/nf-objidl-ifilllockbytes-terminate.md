---
UID: NF:objidl.IFillLockBytes.Terminate
title: IFillLockBytes::Terminate
author: windows-sdk-content
description: The Terminate method informs the byte array that the download has been terminated, either successfully or unsuccessfully.
old-location: stg\ifilllockbytes_terminate.htm
old-project: Stg
ms.assetid: 21ea78c7-51f1-4418-915c-79db47c25715
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IFillLockBytes interface [Structured Storage],Terminate method, IFillLockBytes.Terminate, IFillLockBytes::Terminate, Terminate, Terminate method [Structured Storage], Terminate method [Structured Storage],IFillLockBytes interface, _stg_ifilllockbytes_terminate, objidl/IFillLockBytes::Terminate, stg.ifilllockbytes_terminate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - IFillLockBytes.Terminate
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



