---
UID: NE:mfobjects._MF2DBuffer_LockFlags
title: MF2DBuffer_LockFlags
author: windows-sdk-content
description: Contains flags for the IMF2DBuffer2::Lock2DSize method.
old-location: mf\mf2dbuffer_lockflags.htm
tech.root: medfound
ms.assetid: 298E3FBE-1902-4AA1-9CC8-5B8D65A48ECF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MF2DBuffer_LockFlags, MF2DBuffer_LockFlags enumeration [Media Foundation], MF2DBuffer_LockFlags_ForceDWORD, MF2DBuffer_LockFlags_LockTypeMask, MF2DBuffer_LockFlags_Read, MF2DBuffer_LockFlags_ReadWrite, MF2DBuffer_LockFlags_Write, mf.mf2dbuffer_lockflags, mfobjects/MF2DBuffer_LockFlags, mfobjects/MF2DBuffer_LockFlags_ForceDWORD, mfobjects/MF2DBuffer_LockFlags_LockTypeMask, mfobjects/MF2DBuffer_LockFlags_Read, mfobjects/MF2DBuffer_LockFlags_ReadWrite, mfobjects/MF2DBuffer_LockFlags_Write
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfobjects.h, Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.idl
api_name:
 - MF2DBuffer_LockFlags
product: Windows
targetos: Windows
req.typenames: MF2DBuffer_LockFlags
req.redist: 
---

# MF2DBuffer_LockFlags enumeration


## -description


Contains flags for the <a href="https://msdn.microsoft.com/84885FEF-7F6D-4BE3-BF63-F9EC0C7E2D88">IMF2DBuffer2::Lock2DSize</a> method.


## -enum-fields




### -field MF2DBuffer_LockFlags_LockTypeMask

Reserved.


### -field MF2DBuffer_LockFlags_Read

Lock the buffer for reading.


### -field MF2DBuffer_LockFlags_Write

Lock the buffer for writing.


### -field MF2DBuffer_LockFlags_ReadWrite

Lock the buffer for both reading and writing.


### -field MF2DBuffer_LockFlags_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

