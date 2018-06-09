---
UID: NE:mfidl._MF_TOPONODE_FLUSH_MODE
title: "_MF_TOPONODE_FLUSH_MODE"
author: windows-sdk-content
description: Defines when a transform in a topology is flushed.
old-location: mf\mf_toponode_flush_mode.htm
old-project: medfound
ms.assetid: e7eec3c1-f4be-4d7f-9d4c-e98a6a05e85a
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MF_TOPONODE_FLUSH_ALWAYS, MF_TOPONODE_FLUSH_MODE, MF_TOPONODE_FLUSH_MODE enumeration [Media Foundation], MF_TOPONODE_FLUSH_NEVER, MF_TOPONODE_FLUSH_SEEK, _MF_TOPONODE_FLUSH_MODE, e7eec3c1-f4be-4d7f-9d4c-e98a6a05e85a, mf.mf_toponode_flush_mode, mfidl/MF_TOPONODE_FLUSH_ALWAYS, mfidl/MF_TOPONODE_FLUSH_MODE, mfidl/MF_TOPONODE_FLUSH_NEVER, mfidl/MF_TOPONODE_FLUSH_SEEK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_TOPONODE_FLUSH_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_TOPONODE_FLUSH_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MF_TOPONODE_FLUSH_MODE enumeration


## -description



Defines when a transform in a topology is flushed.




## -enum-fields




### -field MF_TOPONODE_FLUSH_ALWAYS

The transform is flushed whenever the stream changes, including seeks and new segments.


### -field MF_TOPONODE_FLUSH_SEEK

The transform is flushed when seeking is performed on the stream.


### -field MF_TOPONODE_FLUSH_NEVER

The transform is never flushed during streaming. It is flushed only when the object is released.


## -see-also




<a href="https://msdn.microsoft.com/1e87f58f-546f-4dd4-b218-1458ff17db53">MF_TOPONODE_FLUSH</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

