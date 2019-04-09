---
UID: NF:winuser.GetAwarenessFromDpiAwarenessContext
title: GetAwarenessFromDpiAwarenessContext function (winuser.h)
author: windows-sdk-content
description: Retrieves the DPI_AWARENESS value from a DPI_AWARENESS_CONTEXT.
old-location: hidpi\getawarenessfromdpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: BE4DC6B9-BCD6-4E27-81F8-E3CF054CFBE9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAwarenessFromDpiAwarenessContext, GetAwarenessFromDpiAwarenessContext function [High DPI], hidpi.getawarenessfromdpiawarenesscontext, winuser/GetAwarenessFromDpiAwarenessContext
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetAwarenessFromDpiAwarenessContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAwarenessFromDpiAwarenessContext function


## -description


Retrieves the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> value from a <b>DPI_AWARENESS_CONTEXT</b>.


## -parameters




### -param value [in]

The <b>DPI_AWARENESS_CONTEXT</b> you want to examine.


## -returns



The <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>. If the provided <i>value</i> is <b>null</b> or invalid, this method will return <b>DPI_AWARENESS_INVALID</b>.




## -remarks



A <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> contains multiple pieces of information. For example, it includes both the current and the inherited <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>. This method retrieves the <b>DPI_AWARENESS</b> from the structure.




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>
 

 

