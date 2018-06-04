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

# tagTextMode enumeration


## -description


Indicates the text mode of a rich edit control. The <a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a> and <a href="https://msdn.microsoft.com/5c976a82-9c51-4700-9db4-a6b0ed7bb852">EM_GETTEXTMODE</a> messages use this enumeration type. 


## -enum-fields




### -field TM_PLAINTEXT

Indicates plain-text mode, in which the control is similar to a standard edit control. For more information about plain-text mode, see the Remarks section of <a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a>. 


### -field TM_RICHTEXT

Indicates rich-text mode, in which the control has the standard rich edit functionality. Rich-text mode is the default setting. 


### -field TM_SINGLELEVELUNDO

The control allows the user to undo only the last action in the undo queue. 


### -field TM_MULTILEVELUNDO

The control supports multiple undo actions. This is the default setting. Use the <a href="https://msdn.microsoft.com/485dbcda-89f4-40de-ad55-cd524958e910">EM_SETUNDOLIMIT</a> message to set the maximum number of undo actions. 


### -field TM_SINGLECODEPAGE

The control only allows the English keyboard and a keyboard corresponding to the default character set. For example, you could have Greek and English. Note that this prevents Unicode text from entering the control. For example, use this value if a Rich Edit control must be restricted to ANSI text.


### -field TM_MULTICODEPAGE

The control allows multiple code pages and Unicode text into the control. This is the default setting.


## -see-also




<a href="https://msdn.microsoft.com/5c976a82-9c51-4700-9db4-a6b0ed7bb852">EM_GETTEXTMODE</a>



<a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a>



<b>Reference</b>
 

 

