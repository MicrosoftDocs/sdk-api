---
UID: NS:naptypes.tagSoHAttribute
title: tagSoHAttribute
author: windows-sdk-content
description: Defines the SoH protocol between the SHA/SHV and the NAP system.
old-location: nap\sohattribute_struct.htm
tech.root: NAP
ms.assetid: cd954277-27e0-47f4-b4c3-f5335925b8fd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SoHAttribute, SoHAttribute structure [NAP], nap.sohattribute_struct, naptypes/SoHAttribute, tagSoHAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
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
 - NapTypes.h
api_name:
 - SoHAttribute
product: Windows
targetos: Windows
req.typenames: SoHAttribute
req.redist: 
---

# tagSoHAttribute structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SoHAttribute</b> structure defines the SoH protocol between the SHA/SHV and the NAP system.


## -struct-fields




### -field type

A <a href="https://msdn.microsoft.com/ba725bf1-1d0a-4489-b912-3e761557d772">SoHAttributeType</a> value that defines the attribute type contained in <b>value</b>. 


### -field size

The size, in bytes, of the SoH attribute pointed to by <b>value</b> and has a range of 0 to <a href="https://msdn.microsoft.com/2727487c-8c6a-4cd9-b6d8-253191a7d7f6">maxSoHAttributeSize</a>.


### -field value

A pointer to a <a href="https://msdn.microsoft.com/53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12">SoHAttributeValue</a> structure that contains the SoH attribute value as defined by <b>type</b>.


## -see-also




<a href="https://msdn.microsoft.com/e391be3c-95ab-4c80-a5d8-8a8fef28e56b">NAP Reference</a>



<a href="https://msdn.microsoft.com/68048587-0f7e-48d4-9326-768a977ea3ee">NAP Structures</a>
 

 

