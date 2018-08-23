---
UID: NF:dwrite.IDWriteTextFormat.SetReadingDirection
title: IDWriteTextFormat::SetReadingDirection
author: windows-sdk-content
description: Sets the paragraph reading direction.
old-location: directwrite\IDWriteTextFormat_SetReadingDirection.htm
old-project: DirectWrite
ms.assetid: fb26241c-e97e-43d3-9f0a-0a9f932d8483
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetReadingDirection method, IDWriteTextFormat.SetReadingDirection, IDWriteTextFormat::SetReadingDirection, SetReadingDirection, SetReadingDirection method [Direct Write], SetReadingDirection method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetReadingDirection, dwrite/IDWriteTextFormat::SetReadingDirection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat.SetReadingDirection
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextFormat::SetReadingDirection


## -description


Sets the paragraph reading direction.


## -parameters




### -param readingDirection

Type: <b><a href="https://msdn.microsoft.com/37288d34-d533-474c-b3c0-8c6361074a9b">DWRITE_READING_DIRECTION</a></b>

The text reading direction (for example, <a href="https://msdn.microsoft.com/37288d34-d533-474c-b3c0-8c6361074a9b">DWRITE_READING_DIRECTION_RIGHT_TO_LEFT</a> for languages, such as 
            Arabic, that read from right to left) for a paragraph.
          


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The reading direction and flow direction must always be set 90 degrees orthogonal to each other, or else you will get the error DWRITE_E_FLOWDIRECTIONCONFLICTS when you 
        use layout functions like Draw or GetMetrics. So if you set a vertical reading direction (for example, to DWRITE_READING_DIRECTION_TOP_TO_BOTTOM), then you must also 
        use SetFlowDirection to set the flow direction appropriately (for example, to DWRITE_FLOW_DIRECTION_RIGHT_TO_LEFT).
      




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

