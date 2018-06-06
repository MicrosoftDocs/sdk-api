---
UID: NE:exdisp.ShellWindowFindWindowOptions
title: ShellWindowFindWindowOptions
author: windows-sdk-content
description: Specifies options for finding window in the Shell windows collection.
old-location: shell\ShellWindowFindWindowOptions.htm
old-project: shell
ms.assetid: 2459ab16-56c0-4812-bc61-4a17978b04f3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SWFO_COOKIEPASSED, SWFO_INCLUDEPENDING, SWFO_NEEDDISPATCH, ShellWindowFindWindowOptions, ShellWindowFindWindowOptions enumeration [Windows Shell], _win32_ShellWindowFindWindowOptions, exdisp/SWFO_COOKIEPASSED, exdisp/SWFO_INCLUDEPENDING, exdisp/SWFO_NEEDDISPATCH, exdisp/ShellWindowFindWindowOptions, shell.ShellWindowFindWindowOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ExDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ShellWindowFindWindowOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ExDisp.h
api_name:
 - ShellWindowFindWindowOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# ShellWindowFindWindowOptions enumeration


## -description



            Specifies options for finding window in the Shell windows collection.
        


## -enum-fields




### -field SWFO_NEEDDISPATCH


            The window must have an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. 
            


### -field SWFO_INCLUDEPENDING


            Include windows that were registered with <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>.
            


### -field SWFO_COOKIEPASSED


            Causes <a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">IShellWindows::FindWindowSW</a> to interpret <i>pvarLoc</i>  as a cookie rather than a PIDL.
            


## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">IShellWindows::FindWindowSW</a>
 

 

