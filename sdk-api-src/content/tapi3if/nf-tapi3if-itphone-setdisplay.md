---
UID: NF:tapi3if.ITPhone.SetDisplay
title: ITPhone::SetDisplay
author: windows-sdk-content
description: The SetDisplay method sets what will appear in a given row and column of the phone's display.
old-location: tapi3\itphone_setdisplay.htm
old-project: Tapi
ms.assetid: 690756c4-201d-472d-b536-452074226701
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITPhone interface [TAPI 2.2],SetDisplay method, ITPhone.SetDisplay, ITPhone::SetDisplay, SetDisplay, SetDisplay method [TAPI 2.2], SetDisplay method [TAPI 2.2],ITPhone interface, _tapi3_itphone_setdisplay, tapi3.itphone_setdisplay, tapi3if/ITPhone::SetDisplay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.SetDisplay
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::SetDisplay


## -description


The 
<b>SetDisplay</b> method sets what will appear in a given row and column of the phone's display.


## -parameters




### -param lRow [in]

Display row.


### -param lColumn [in]

Display column.


### -param bstrDisplay [in]

The <b>BSTR</b> representation of the value to display.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/259982d7-8c28-4c0d-81b3-e4ec49fc9765">get_Display</a>
 

 

