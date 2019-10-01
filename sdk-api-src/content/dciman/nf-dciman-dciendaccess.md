---
UID: NF:dciman.DCIEndAccess
title: DCIEndAccess function (dciman.h)
author: windows-sdk-content
description: Releases access to display frame buffer.
old-location: winprog\_dciman_dciendaccess.htm
tech.root: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\dciendaccess.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DCIEndAccess, DCIEndAccess function [Windows API], _dciman_dciendaccess, dciman/DCIEndAccess, winprog._dciman_dciendaccess, winui._dciman_dciendaccess
ms.topic: function
f1_keywords: 
 - "dciman/DCIEndAccess"
req.header: dciman.h
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
req.lib: Dciman32.lib
req.dll: Dciman32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dciman32.dll
api_name:
 - DCIEndAccess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DCIEndAccess function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Releases access to display frame buffer.



## -parameters




### -param pdci [in]

A pointer to a <b>DCISURFACEINFO</b> structure.
 


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>
 

 

