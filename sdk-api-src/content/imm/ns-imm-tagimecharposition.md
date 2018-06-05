---
UID: NS:imm.tagIMECHARPOSITION
title: tagIMECHARPOSITION
author: windows-sdk-content
description: Contains information about the character position in the composition window.
old-location: intl\imecharposition.htm
old-project: Intl
ms.assetid: 5c278df0-ce90-4f9d-915e-45dadc823360
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPIMECHARPOSITION, *NPIMECHARPOSITION, *PIMECHARPOSITION, IMECHARPOSITION, IMECHARPOSITION structure [Internationalization for Windows Applications], PIMECHARPOSITION, PIMECHARPOSITION structure pointer [Internationalization for Windows Applications], _win32_IMECHARPOSITION_str, imm/IMECHARPOSITION, imm/PIMECHARPOSITION, intl.imecharposition, tagIMECHARPOSITION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IMECHARPOSITION, *PIMECHARPOSITION, *NPIMECHARPOSITION, *LPIMECHARPOSITION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Imm.h
api_name:
-	IMECHARPOSITION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagIMECHARPOSITION structure


## -description



Contains information about the character position in the composition window.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwCharPos

Character offset in the composition string, in <b>TCHAR</b> values.


### -field pt

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure containing the coordinate of the top left point of requested character in screen coordinates. The top left point is based on the character baseline in any text flow.


### -field cLineHeight

Height of a line that contains the requested character, in pixels.


### -field rcDocument

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the editable area for text, in screen coordinates, for the application.


## -remarks



When an application uses IME to draw the composition string, the members of this structure are automatically filled. Applications that draw the composition string themselves, rather than relying on the IME, are responsible for filling all the fields defined in the structure.




## -see-also




<a href="https://msdn.microsoft.com/cae7e5b3-8aaf-452d-80df-fb0ae04a342c">IMR_QUERYCHARPOSITION</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/1be3ae8b-e083-4420-bc8a-7f49c4264cab">Input Method Manager Structures</a>
 

 

