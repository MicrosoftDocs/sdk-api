---
UID: NF:shimgdata.IShellImageDataAbort.QueryAbort
title: IShellImageDataAbort::QueryAbort
author: windows-sdk-content
description: Aborts an IShellImageData process such as Decode, Draw, or Scale. This is a callback method.
old-location: shell\IShellImageDataAbort_QueryAbort.htm
old-project: shell
ms.assetid: 88823fe3-efde-4ee1-9b4f-685f8df03b29
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IShellImageDataAbort interface [Windows Shell],QueryAbort method, IShellImageDataAbort.QueryAbort, IShellImageDataAbort::QueryAbort, QueryAbort, QueryAbort method [Windows Shell], QueryAbort method [Windows Shell],IShellImageDataAbort interface, _shell_IShellImageDataAbort_QueryAbort, shell.IShellImageDataAbort_QueryAbort, shimgdata/IShellImageDataAbort::QueryAbort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellImageDataAbort.QueryAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageDataAbort::QueryAbort


## -description


Aborts an <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> process such as <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">Decode</a>, <a href="https://msdn.microsoft.com/35989c3b-15b9-4503-a883-99df730b2a80">Draw</a>, or <a href="https://msdn.microsoft.com/ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434">Scale</a>. This is a callback method.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> process should continue, or S_FALSE if it should be aborted.



