---
UID: NF:commctrl.INDEXTOSTATEIMAGEMASK
title: INDEXTOSTATEIMAGEMASK macro
author: windows-sdk-content
description: Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item.
old-location: controls\INDEXTOSTATEIMAGEMASK.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\macros\indextostateimagemask.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INDEXTOSTATEIMAGEMASK, INDEXTOSTATEIMAGEMASK macro [Windows Controls], _win32_INDEXTOSTATEIMAGEMASK, _win32_INDEXTOSTATEIMAGEMASK_cpp, commctrl/INDEXTOSTATEIMAGEMASK, controls.INDEXTOSTATEIMAGEMASK, controls._win32_INDEXTOSTATEIMAGEMASK
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - INDEXTOSTATEIMAGEMASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# INDEXTOSTATEIMAGEMASK macro


## -description


Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item. 


## -parameters




### -param i

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of a state image. 


## -remarks



The <b>INDEXTOSTATEIMAGEMASK</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define INDEXTOSTATEIMAGEMASK(i) ((i) &lt;&lt; 12)</code></pre>


