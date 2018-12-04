---
UID: NF:dwrite.IDWriteTextLayout.GetLineMetrics
title: IDWriteTextLayout::GetLineMetrics
author: windows-sdk-content
description: Retrieves the information about each individual text line of the text string.
old-location: directwrite\IDWriteTextLayout_GetLineMetrics.htm
tech.root: DirectWrite
ms.assetid: 30f49632-d7fa-44e2-b289-2ad658e0c867
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetLineMetrics, GetLineMetrics method [Direct Write], GetLineMetrics method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetLineMetrics method, IDWriteTextLayout.GetLineMetrics, IDWriteTextLayout::GetLineMetrics, directwrite.IDWriteTextLayout_GetLineMetrics, dwrite/IDWriteTextLayout::GetLineMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout.GetLineMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetLineMetrics


## -description


Retrieves the information about each individual text line of the  text string.


## -parameters




### -param lineMetrics [out, optional]

Type: <b><a href="https://msdn.microsoft.com/cb589949-2eba-4ebb-ada4-546802fb3d01">DWRITE_LINE_METRICS</a>*</b>

When this method returns, contains a pointer to an array of structures containing various calculated length values of individual text lines.


### -param maxLineCount

Type: <b>UINT32</b>

The maximum size of the <i>lineMetrics</i> array.


### -param actualLineCount [out]

Type: <b>UINT32*</b>

When this method returns, contains the actual size of the <i>lineMetrics</i>array that is needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If <i>maxLineCount</i> is not large enough E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), is
     returned and <i>*actualLineCount</i> is set to the number of lines
     needed.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

