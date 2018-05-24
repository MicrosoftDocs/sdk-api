---
UID: NS:winnt._LUID
title: "_LUID"
author: windows-driver-content
description: 64-bit value guaranteed to be unique only on the system on which it was generated.
old-location: security\luid.htm
old-project: SecAuthZ
ms.assetid: a812a46b-f23f-45b1-a6c6-48f931b78750
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*PLUID, LUID, LUID structure [Security], PLUID, PLUID structure pointer [Security], _LUID, _win32_luid_str, security.luid, winnt/LUID, winnt/PLUID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: LUID, *PLUID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	LUID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _LUID structure


## -description


An <b>LUID</b> is a 64-bit value guaranteed to be unique only on the system on which it was generated. The uniqueness of a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) is guaranteed only until the system is restarted.

Applications must use functions and structures to manipulate <b>LUID</b> values.


## -struct-fields




### -field LowPart

Low-order bits.


### -field HighPart

High-order bits.


## -see-also




<a href="https://msdn.microsoft.com/5d730034-802b-4d37-bd28-68992779b93e">AllocateLocallyUniqueId</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549716">LUID_AND_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/580fb58f-1470-4389-9f07-8f37403e2bdf">LookupPrivilegeName</a>



<a href="https://msdn.microsoft.com/334b8ba8-101d-43a1-a8bf-1c7e0448c272">LookupPrivilegeValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551860">PRIVILEGE_SET</a>



<a href="https://msdn.microsoft.com/a73d934a-1abf-4e60-bf0a-6c4629f28f7a">PrivilegeCheck</a>
 

 

