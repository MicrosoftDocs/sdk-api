---
UID: NS:winuser.tagRAWHID
title: tagRAWHID
author: windows-sdk-content
description: Describes the format of the raw input from a Human Interface Device (HID).
old-location: inputdev\rawhid.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawhid.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*LPRAWHID, *PRAWHID, LPRAWHID, LPRAWHID structure pointer [Keyboard and Mouse Input], PRAWHID, PRAWHID structure pointer [Keyboard and Mouse Input], RAWHID, RAWHID structure [Keyboard and Mouse Input], _win32_RAWHID_str, _win32_rawhid_str_cpp, inputdev.rawhid, tagRAWHID, winui._win32_rawhid_str, winuser/LPRAWHID, winuser/PRAWHID, winuser/RAWHID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWHID
product: Windows
targetos: Windows
req.typenames: RAWHID, *PRAWHID, *LPRAWHID
req.redist: 
---

# tagRAWHID structure


## -description


Describes the format of the raw input from a Human Interface Device (HID). 


## -struct-fields




### -field dwSizeHid

Type: <b>DWORD</b>

The size, in bytes, of each HID input in <b>bRawData</b>. 


### -field dwCount

Type: <b>DWORD</b>

The number of HID inputs in <b>bRawData</b>.


### -field bRawData

Type: <b>BYTE[1]</b>

The raw input data, as an array of bytes. 


## -remarks



Each <a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a> can indicate several inputs, but all of the inputs come from the same HID. The size of the <b>bRawData</b> array is <b>dwSizeHid</b> *	<b>dwCount</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>
 

 

