---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IImageList2::GetOriginalSize


## -description


Gets the original size of a specified image.


## -parameters




### -param iImage [in]

Type: <b>int</b>

The index of desired image.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flags for getting original size. One of the following is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILGOS_ALWAYS"></a><a id="ilgos_always"></a><dl>
<dt><b>ILGOS_ALWAYS</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Always get the original size (can be slow). 

</td>
</tr>
<tr>
<td width="40%"><a id="ILGOS_FROMSTANDBY"></a><a id="ilgos_fromstandby"></a><dl>
<dt><b>ILGOS_FROMSTANDBY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Only get if present or on standby. 

</td>
</tr>
</table>
 


### -param pcx [out]

Type: <b>int*</b>

A pointer to the x-axis count.


### -param pcy [out]

Type: <b>int*</b>

A pointer to the y-axis count.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



