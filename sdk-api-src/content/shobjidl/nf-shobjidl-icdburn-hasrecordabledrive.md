---
UID: NF:shobjidl.ICDBurn.HasRecordableDrive
title: ICDBurn::HasRecordableDrive
author: windows-sdk-content
description: Scans the system for a CD drive with write-capability, returning TRUE if one is found.
old-location: shell\ICDBurn_HasRecordableDrive.htm
tech.root: shell
ms.assetid: b20b5242-2d38-4f86-9267-a2211ef07a00
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: HasRecordableDrive, HasRecordableDrive method [Windows Shell], HasRecordableDrive method [Windows Shell],ICDBurn interface, ICDBurn interface [Windows Shell],HasRecordableDrive method, ICDBurn.HasRecordableDrive, ICDBurn::HasRecordableDrive, _shell_ICDBurn_HasRecordableDrive, shell.ICDBurn_HasRecordableDrive, shobjidl/ICDBurn::HasRecordableDrive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICDBurn.HasRecordableDrive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDBurn::HasRecordableDrive


## -description


Scans the system for a CD drive with write-capability, returning <b>TRUE</b> if one is found.


## -parameters




### -param pfHasRecorder [out]

Type: <b>BOOL*</b>

A pointer to a Boolean value containing <b>TRUE</b> if a suitable device is located, <b>FALSE</b> otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This search does not rely on the state of the <b>Enable cd writing on this drive</b> option found on the drive's property sheet. Instead, the determination is based on IMAPI.



