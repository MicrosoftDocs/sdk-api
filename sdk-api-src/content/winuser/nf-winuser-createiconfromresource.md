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

# CreateIconFromResource function


## -description


Creates an icon or cursor from resource bits describing the icon.

To specify a desired height or width, use the <a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a> function.


## -parameters




### -param presbits [in]

Type: <b>PBYTE</b>

The buffer containing the icon or cursor resource bits. These bits are typically loaded by calls to the <a href="https://msdn.microsoft.com/4a934e23-597e-48c3-a5f4-9bcf6713dda6">LookupIconIdFromDirectory</a>, <a href="https://msdn.microsoft.com/5ab25565-30a5-4d4f-bf41-2ce3948d6f2f">LookupIconIdFromDirectoryEx</a>, and <a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a> functions. 


### -param dwResSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the set of bits pointed to by the <i>presbits</i> parameter. 


### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is to be created. If this parameter is <b>TRUE</b>, an icon is to be created. If it is <b>FALSE</b>, a cursor is to be created. 


### -param dwVer [in]

Type: <b>DWORD</b>

The version number of the icon or cursor format for the resource bits pointed to by the <i>presbits</i> parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CreateIconFromResource</b>, <a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a>, <a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>, <a href="https://msdn.microsoft.com/94cc619b-1ca8-4268-9af3-d10d221e093e">GetIconInfo</a>, <a href="https://msdn.microsoft.com/4a934e23-597e-48c3-a5f4-9bcf6713dda6">LookupIconIdFromDirectory</a>, and <a href="https://msdn.microsoft.com/5ab25565-30a5-4d4f-bf41-2ce3948d6f2f">LookupIconIdFromDirectoryEx</a> functions allow shell applications and icon browsers to examine and use resources throughout the system. 

The <b>CreateIconFromResource</b> function calls <a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a> passing <code>LR_DEFAULTSIZE|LR_SHARED</code> as flags.

When you are finished using the icon, destroy it using the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a>



<a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/94cc619b-1ca8-4268-9af3-d10d221e093e">GetIconInfo</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<a href="https://msdn.microsoft.com/4c91f571-505d-4959-b337-8f26c91fc573">LoadResource</a>



<a href="https://msdn.microsoft.com/4a934e23-597e-48c3-a5f4-9bcf6713dda6">LookupIconIdFromDirectory</a>



<a href="https://msdn.microsoft.com/5ab25565-30a5-4d4f-bf41-2ce3948d6f2f">LookupIconIdFromDirectoryEx</a>



<b>Reference</b>
 

 

