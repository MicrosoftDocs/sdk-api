---
UID: NE:docobj.__unnamed_enum_5
title: OLECMDID_WINDOWSTATE_FLAG (docobj.h)
author: windows-sdk-content
description: Specifies the window state.
old-location: com\olecmdid_windowstate_flag.htm
tech.root: com
ms.assetid: 31331c73-1f26-436d-8fa7-83f13ef51f0e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OLECMDIDF_WINDOWSTATE_ENABLED, OLECMDIDF_WINDOWSTATE_ENABLED_VALID, OLECMDIDF_WINDOWSTATE_USERVISIBLE, OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID, OLECMDID_WINDOWSTATE_FLAG, OLECMDID_WINDOWSTATE_FLAG enumeration [COM], _ole_OLECMDID_WINDOWSTATE_FLAG, com.olecmdid_windowstate_flag, docobj/OLECMDIDF_WINDOWSTATE_ENABLED, docobj/OLECMDIDF_WINDOWSTATE_ENABLED_VALID, docobj/OLECMDIDF_WINDOWSTATE_USERVISIBLE, docobj/OLECMDIDF_WINDOWSTATE_USERVISIBLE_VALID, docobj/OLECMDID_WINDOWSTATE_FLAG
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: OLECMDID_WINDOWSTATE_FLAG
req.redist: 
ms.custom: 19H1
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



A value from this enumeration is passed as the <i>nCmdExecOpt</i> parameter to <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a> in conjunction with passing the OLECMDID_WINDOWSTATECHANGED value of the <a href="https://docs.microsoft.com/windows/desktop/api/docobj/ne-docobj-olecmdid">OLECMDID</a> enumeration as the <i>nCmdID</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/ne-docobj-olecmdid">OLECMDID</a>
 

 

