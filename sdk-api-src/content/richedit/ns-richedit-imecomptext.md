---
UID: NS:richedit._imecomptext
title: IMECOMPTEXT (richedit.h)
author: windows-sdk-content
description: Contains information about the Input Method Editor (IME) composition text in a Microsoft Rich Edit control.
old-location: controls\IMECOMPTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\imecomptext.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICT_RESULTREADSTR, IMECOMPTEXT, IMECOMPTEXT structure [Windows Controls], _win32_IMECOMPTEXT_str, _win32_IMECOMPTEXT_str_cpp, controls.IMECOMPTEXT, controls._win32_IMECOMPTEXT_str, richedit/IMECOMPTEXT
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMECOMPTEXT
product: Windows
targetos: Windows
req.typenames: IMECOMPTEXT
req.redist: 
ms.custom: 19H1
---

# IMECOMPTEXT structure


## -description


Contains information about the Input Method Editor (IME) composition text in a Microsoft Rich Edit control.
		


## -struct-fields




### -field cb

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Size of the output buffer, in bytes. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Type of composition string. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICT_RESULTREADSTR"></a><a id="ict_resultreadstr"></a><dl>
<dt><b>ICT_RESULTREADSTR</b></dt>
</dl>
</td>
<td width="60%">
The final composed string.

</td>
</tr>
</table>
 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/1516305c-5f87-4ae0-97db-8709c71abacc">EM_GETIMECOMPTEXT</a> message.




## -see-also




<a href="https://msdn.microsoft.com/1516305c-5f87-4ae0-97db-8709c71abacc">EM_GETIMECOMPTEXT</a>
 

 

