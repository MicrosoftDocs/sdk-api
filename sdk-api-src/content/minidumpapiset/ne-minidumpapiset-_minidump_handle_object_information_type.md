---
UID: NE:minidumpapiset._MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
title: "_MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE"
author: windows-sdk-content
description: Identifies the type of object-specific information.
old-location: base\minidump_handle_object_information_type.htm
old-project: debug
ms.assetid: 255023e3-0412-42c8-ae80-eba5f00af5ff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE, MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration, MiniHandleObjectInformationNone, MiniMutantInformation1, MiniMutantInformation2, MiniProcessInformation1, MiniProcessInformation2, MiniThreadInformation1, _MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE, base.minidump_handle_object_information_type, minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE, minidumpapiset/MiniHandleObjectInformationNone, minidumpapiset/MiniMutantInformation1, minidumpapiset/MiniMutantInformation2, minidumpapiset/MiniProcessInformation1, minidumpapiset/MiniProcessInformation2, minidumpapiset/MiniThreadInformation1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 6.5 or later
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE enumeration


## -description


Identifies the type of object-specific information.


## -enum-fields




### -field MiniHandleObjectInformationNone

There is no object-specific information for this handle type.


### -field MiniThreadInformation1

The information is specific to thread objects.


### -field MiniMutantInformation1

The information is specific to mutant objects.


### -field MiniMutantInformation2

The information is specific to mutant objects.


### -field MiniProcessInformation1

The information is specific to process objects.


### -field MiniProcessInformation2

The information is specific to process objects.


### -field MiniEventInformation1


### -field MiniSectionInformation1


### -field MiniSemaphoreInformation1


### -field MiniHandleObjectInformationTypeMax




## -remarks



The information represented by each of these values can vary by operating system and procesor architecture. Per-handle object-specific information is automatically gathered when minidump type is MiniDumpWithHandleData. For more information, see <a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb79de10-7a98-4a21-b394-63e5279b6681">MINIDUMP_HANDLE_OBJECT_INFORMATION</a>
 

 

