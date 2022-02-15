---
UID: NF:shobjidl.IStreamUnbufferedInfo.GetSectorSize
title: IStreamUnbufferedInfo::GetSectorSize (shobjidl.h)
description: Retrieves the number of bytes per sector on the disk currently being used. When using unbuffered input/output (I/O), it is important to know the size of the sectors on the disk being read in order to ensure proper byte alignment.
helpviewer_keywords: ["GetSectorSize","GetSectorSize method [Windows Shell]","GetSectorSize method [Windows Shell]","IStreamUnbufferedInfo interface","IStreamUnbufferedInfo interface [Windows Shell]","GetSectorSize method","IStreamUnbufferedInfo.GetSectorSize","IStreamUnbufferedInfo::GetSectorSize","_shell_IStreamUnbufferedInfo_GetSectorSize","shell.IStreamUnbufferedInfo_GetSectorSize","shobjidl/IStreamUnbufferedInfo::GetSectorSize"]
old-location: shell\IStreamUnbufferedInfo_GetSectorSize.htm
tech.root: shell
ms.assetid: 2194de8b-25bd-4eeb-8a67-d5bd22947497
ms.date: 12/05/2018
ms.keywords: GetSectorSize, GetSectorSize method [Windows Shell], GetSectorSize method [Windows Shell],IStreamUnbufferedInfo interface, IStreamUnbufferedInfo interface [Windows Shell],GetSectorSize method, IStreamUnbufferedInfo.GetSectorSize, IStreamUnbufferedInfo::GetSectorSize, _shell_IStreamUnbufferedInfo_GetSectorSize, shell.IStreamUnbufferedInfo_GetSectorSize, shobjidl/IStreamUnbufferedInfo::GetSectorSize
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamUnbufferedInfo::GetSectorSize
 - shobjidl/IStreamUnbufferedInfo::GetSectorSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IStreamUnbufferedInfo.GetSectorSize
---

# IStreamUnbufferedInfo::GetSectorSize


## -description

Retrieves the number of bytes per sector on the disk currently being used.  When using unbuffered input/output (I/O), it is important to know the size of the sectors on the disk being read in order to ensure proper byte alignment.

## -parameters

### -param pcbSectorSize [out]

Type: <b>ULONG*</b>

When this method returns successfully, contains a pointer to a <b>ULONG</b> value that represents the number of bytes per sector for the disk.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

