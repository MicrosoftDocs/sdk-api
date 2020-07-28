---
UID: NF:recapis.GetAllRecognizers
title: GetAllRecognizers function (recapis.h)
description: Gets all recognizers.
helpviewer_keywords: ["GetAllRecognizers","GetAllRecognizers function [Tablet PC]","recapis/GetAllRecognizers","tablet.getallrecognizers"]
old-location: tablet\getallrecognizers.htm
tech.root: tablet
ms.assetid: F2039094-E3B0-4FF4-9B69-ED29D681B388
ms.date: 12/05/2018
ms.keywords: GetAllRecognizers, GetAllRecognizers function [Tablet PC], recapis/GetAllRecognizers, tablet.getallrecognizers
f1_keywords:
- recapis/GetAllRecognizers
dev_langs:
- c++
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- recapis.h
api_name:
- GetAllRecognizers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetAllRecognizers function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Gets all recognizers.


## -parameters




### -param recognizerClsids

Pointer to the CLSIDs of the recognizers. The CLSID value is created in the registry when you register the recognizer.


### -param count

Pointer to the number of recognizers.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 



