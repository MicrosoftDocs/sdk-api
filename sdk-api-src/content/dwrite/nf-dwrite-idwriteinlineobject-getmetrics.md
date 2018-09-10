---
UID: NF:dwrite.IDWriteInlineObject.GetMetrics
title: IDWriteInlineObject::GetMetrics
author: windows-sdk-content
description: IDWriteTextLayout calls this callback function to get the measurement of the inline object.
old-location: directwrite\IDWriteInlineObject_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 809a4e29-0423-40b2-9d40-105d30574fa1
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],GetMetrics method, IDWriteInlineObject.GetMetrics, IDWriteInlineObject::GetMetrics, directwrite.IDWriteInlineObject_GetMetrics, dwrite/IDWriteInlineObject::GetMetrics
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
 - IDWriteInlineObject.GetMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteInlineObject::GetMetrics


## -description



<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> calls this callback function to get the measurement of the inline object.


## -parameters




### -param metrics [out]

Type: <b><a href="https://msdn.microsoft.com/a42d612c-3d16-4c27-a1d8-1cfb9de2f8b1">DWRITE_INLINE_OBJECT_METRICS</a>*</b>

When this method returns, contains a structure describing the geometric measurement of an
application-defined inline object.  These metrics are in relation to the baseline of the adjacent text. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>
 

 

