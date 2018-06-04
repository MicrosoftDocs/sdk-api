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

# ITextHost2::TxGetEastAsianFlags


## -description


Gets whether Input Method Editor (IME) input is allowed and whether the edit styles include <a href="Rich_Edit_Control_Styles.htm">ES_SELFIME</a>.


## -parameters




### -param pFlags

Type: <b>LONG*</b>

The East Asian flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ES_NOIME"></a><a id="es_noime"></a><dl>
<dt><b><a href="Rich_Edit_Control_Styles.htm">ES_NOIME</a></b></dt>
</dl>
</td>
<td width="60%">
IME input is suppressed.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_SELFIME"></a><a id="es_selfime"></a><dl>
<dt><b><a href="Rich_Edit_Control_Styles.htm">ES_SELFIME</a></b></dt>
</dl>
</td>
<td width="60%">
The rich edit client handles IME imput.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

