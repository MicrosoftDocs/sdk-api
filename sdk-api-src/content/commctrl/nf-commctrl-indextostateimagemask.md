---
UID: NF:commctrl.INDEXTOSTATEIMAGEMASK
title: INDEXTOSTATEIMAGEMASK macro
author: windows-sdk-content
description: Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item.
old-location: controls\INDEXTOSTATEIMAGEMASK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\macros\indextostateimagemask.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: INDEXTOSTATEIMAGEMASK, INDEXTOSTATEIMAGEMASK macro [Windows Controls], _win32_INDEXTOSTATEIMAGEMASK, _win32_INDEXTOSTATEIMAGEMASK_cpp, commctrl/INDEXTOSTATEIMAGEMASK, controls.INDEXTOSTATEIMAGEMASK, controls._win32_INDEXTOSTATEIMAGEMASK
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
 - INDEXTOSTATEIMAGEMASK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INDEXTOSTATEIMAGEMASK macro


## -description


Prepares the index of a state image so that a tree-view control or list-view control can use the index to retrieve the state image for an item. 


## -parameters




### -param i

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The index of a state image. 


## -remarks



The <b>INDEXTOSTATEIMAGEMASK</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define INDEXTOSTATEIMAGEMASK(i) ((i) &lt;&lt; 12)</code></pre>


