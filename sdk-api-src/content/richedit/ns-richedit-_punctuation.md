---
UID: NS:richedit._punctuation
title: "_punctuation"
author: windows-sdk-content
description: Contains information about the punctuation used in a rich edit control.
old-location: controls\PUNCTUATION.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\punctuation.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: PUNCTUATION, PUNCTUATION structure [Windows Controls], _punctuation, _win32_PUNCTUATION_str, _win32_PUNCTUATION_str_cpp, controls.PUNCTUATION, controls._win32_PUNCTUATION_str, richedit/PUNCTUATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - Richedit.h
api_name:
 - PUNCTUATION
product: Windows
targetos: Windows
req.typenames: PUNCTUATION
req.redist: 
---

# _punctuation structure


## -description


Contains information about the punctuation used in a rich edit control.


## -struct-fields




### -field iSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of buffer pointed to by the 
					<b>szPunctuation</b> member, in bytes. 


### -field szPunctuation

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

The buffer containing the punctuation characters. 


## -remarks



This structure is used only in Asian-language versions of the operating system.




## -see-also




<a href="https://msdn.microsoft.com/1c04967b-d75e-4f54-b35b-cd50bac9cdfa">EM_GETPUNCTUATION</a>



<a href="https://msdn.microsoft.com/c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522">EM_SETPUNCTUATION</a>



<b>Reference</b>
 

 

