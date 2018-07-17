---
UID: NE:docobj.OLECMDID_WINDOWSTATE_FLAG
title: OLECMDID_WINDOWSTATE_FLAG
author: windows-sdk-content
description: Specifies the window state.
old-location: com\olecmdid_windowstate_flag.htm
old-project: com
ms.assetid: 31331c73-1f26-436d-8fa7-83f13ef51f0e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: OLECMDIDF_WINDOWSTATE_ENABLED, OLECMDIDF_WINDOWSTATE_ENABLED_VALID, OLECMDIDF_WINDOWSTATE_USERVISIBLE, OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID, OLECMDID_WINDOWSTATE_FLAG, OLECMDID_WINDOWSTATE_FLAG enumeration [COM], _ole_OLECMDID_WINDOWSTATE_FLAG, com.olecmdid_windowstate_flag, docobj/OLECMDIDF_WINDOWSTATE_ENABLED, docobj/OLECMDIDF_WINDOWSTATE_ENABLED_VALID, docobj/OLECMDIDF_WINDOWSTATE_USERVISIBLE, docobj/OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID, docobj/OLECMDID_WINDOWSTATE_FLAG
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: docobj.h
req.include-header: 
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
req.typenames: OLECMDID_WINDOWSTATE_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - OLECMDID_WINDOWSTATE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# OLECMDID_WINDOWSTATE_FLAG enumeration


## -description


Specifies the window state.


## -enum-fields




### -field OLECMDIDF_WINDOWSTATE_USERVISIBLE

The window is visible.


### -field OLECMDIDF_WINDOWSTATE_ENABLED

The window has focus.


### -field OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID

The window is visible and valid.


### -field OLECMDIDF_WINDOWSTATE_ENABLED_VALID

The window has focus and is valid.


## -remarks



A value from this enumeration is passed as the <i>nCmdExecOpt</i> parameter to <a href="https://msdn.microsoft.com/a2071ca9-8675-4f53-b30e-8c7198c2acca">IOleCommandTarget::Exec</a> in conjunction with passing the OLECMDID_WINDOWSTATECHANGED value of the <a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a> enumeration as the <i>nCmdID</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/ae1592b6-2afd-4379-a18e-d46b226bc9e2">OLECMDID</a>
 

 

