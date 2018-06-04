---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# RtlConvertSidToUnicodeString function


## -description


<p class="CCE_Message">[The <b>RtlConvertSidToUnicodeString</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/e673e727-edb1-450c-9e1a-a3dc90acc929">ConvertSidToStringSid</a> function.]

The <b>RtlConvertSidToUnicodeString</b> function converts a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) to its Unicode character representation. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.


## -parameters




### -param UnicodeString [out]

A pointer to the Unicode character representation of the security identifier.


### -param Sid [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that represents the security identifier.


### -param AllocateDestinationString [in]

If <b>TRUE</b>, then  <i>UnicodeString</i> is allocated on behalf of the caller, and it is the caller's responsibility to free the allocated memory by calling the <b>RtlFreeUnicodeString</b> function. If <b>FALSE</b>, the caller is responsible for allocating and freeing  <i>UnicodeString</i>.


## -returns



The return value is an  NTSTATUS code. A value of STATUS_SUCCESS (0x00000000L) is returned if the function succeeds.



