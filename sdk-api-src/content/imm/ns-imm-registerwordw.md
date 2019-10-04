---
UID: NS:imm.tagREGISTERWORDW
title: REGISTERWORDW (imm.h)
author: windows-sdk-content
description: Contains reading information or a word to register.
old-location: intl\registerword.htm
tech.root: Intl
ms.assetid: 70a11a96-a0e3-4741-be91-b85eb38cd767
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPREGISTERWORDW, *NPREGISTERWORDW, *PREGISTERWORDW, PREGISTERWORD, PREGISTERWORD structure pointer [Internationalization for Windows Applications], REGISTERWORD, REGISTERWORD structure [Internationalization for Windows Applications], REGISTERWORDA, REGISTERWORDW, _win32_REGISTERWORD_str, imm/PREGISTERWORD, imm/REGISTERWORD, imm/REGISTERWORDA, imm/REGISTERWORDW, intl.registerword, tagREGISTERWORDA, tagREGISTERWORDW"
ms.topic: struct
f1_keywords: 
 - "imm/REGISTERWORD"
dev_langs:
 - c++
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: REGISTERWORDW (Unicode) and REGISTERWORDA (ANSI)
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
 - Imm.h
api_name:
 - REGISTERWORD
 - REGISTERWORDA
 - REGISTERWORDW
targetos: Windows
req.typenames: REGISTERWORDW, *PREGISTERWORDW, *NPREGISTERWORDW, *LPREGISTERWORDW
req.redist: 
ms.custom: 19H1
---

# REGISTERWORDW structure


## -description



Contains reading information or a word to register.




## -struct-fields




### -field lpReading

Pointer to the reading information for the word to register. If the reading information is not needed, the member can be set to <b>NULL</b>.


### -field lpWord

Pointer to the word to register. If a word is not needed, the member can be set to <b>NULL</b>.


## -remarks



The application can pass this structure to the <a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immconfigureimea">ImmConfigureIME</a> function to have the information or word appear as an initial value in the configuration dialog box for the IME.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imm/nf-imm-immconfigureimea">ImmConfigureIME</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>
 

 

