---
UID: NF:commctrl.INDEXTOSTATEIMAGEMASK
title: INDEXTOSTATEIMAGEMASK macro (commctrl.h)
description: Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item.
old-location: controls\INDEXTOSTATEIMAGEMASK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\indextostateimagemask.htm
ms.date: 12/05/2018
ms.keywords: INDEXTOSTATEIMAGEMASK, INDEXTOSTATEIMAGEMASK macro [Windows Controls], _win32_INDEXTOSTATEIMAGEMASK, _win32_INDEXTOSTATEIMAGEMASK_cpp, commctrl/INDEXTOSTATEIMAGEMASK, controls.INDEXTOSTATEIMAGEMASK, controls._win32_INDEXTOSTATEIMAGEMASK
f1_keywords:
- commctrl/INDEXTOSTATEIMAGEMASK
dev_langs:
- c++
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
- INDEXTOSTATEIMAGEMASK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INDEXTOSTATEIMAGEMASK macro


## -description


Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item. 


## -parameters




### -param i

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of a state image. 


## -remarks



The <b>INDEXTOSTATEIMAGEMASK</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define INDEXTOSTATEIMAGEMASK(i) ((i) &lt;&lt; 12)</code></pre>


