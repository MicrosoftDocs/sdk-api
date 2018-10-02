---
UID: NF:commctrl.INDEXTOOVERLAYMASK
title: INDEXTOOVERLAYMASK macro
author: windows-sdk-content
description: Prepares the index of an overlay mask so that the ImageList_Draw function can use it.
old-location: controls\INDEXTOOVERLAYMASK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\indextooverlaymask.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: INDEXTOOVERLAYMASK, INDEXTOOVERLAYMASK macro [Windows Controls], _win32_INDEXTOOVERLAYMASK, _win32_INDEXTOOVERLAYMASK_cpp, commctrl/INDEXTOOVERLAYMASK, controls.INDEXTOOVERLAYMASK, controls._win32_INDEXTOOVERLAYMASK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - INDEXTOOVERLAYMASK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INDEXTOOVERLAYMASK macro


## -description


Prepares the index of an overlay mask so that the <a href="https://msdn.microsoft.com/d50d94e4-89cb-4992-b98b-84b22ff11191">ImageList_Draw</a> function can use it. 


## -parameters




### -param i

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An index of an overlay mask. 


## -remarks



The <b>INDEXTOOVERLAYMASK</b> macro is defined as follows.


<pre class="syntax" xml:space="preserve"><code>#define INDEXTOOVERLAYMASK(i) ((i) &lt;&lt; 8)</code></pre>


