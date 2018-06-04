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

# tagIMECOMPOSITIONSTRINGINFO structure


## -description


Contains information of IME's composition string in an app.


## -struct-fields




### -field iCompStrLen

Length (number of <b>WCHAR</b>s) of composition string.


### -field iCaretPos

Caret position of composition string.


### -field iEditStart

Position of composition string that is editable.


### -field iEditLen

Length of composition string that is editable.


### -field iTargetStart

Start position of target phrase of composition string.


### -field iTargetLen

Target phrase length of composition string.


## -see-also




<a href="https://msdn.microsoft.com/C74B0374-D6C7-44C7-94EF-E97B46534462">IImePad::Request</a>
 

 

