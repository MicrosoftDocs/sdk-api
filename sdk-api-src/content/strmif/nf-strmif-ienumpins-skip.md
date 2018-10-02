---
UID: NF:strmif.IEnumPins.Skip
title: IEnumPins::Skip
author: windows-sdk-content
description: The Skip method skips over a specified number of pins.
old-location: dshow\ienumpins_skip.htm
tech.root: DirectShow
ms.assetid: 501d08ee-ebd1-48dc-8cc9-bf017034b4cd
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IEnumPins interface [DirectShow],Skip method, IEnumPins.Skip, IEnumPins::Skip, IEnumPinsSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumPins interface, dshow.ienumpins_skip, strmif/IEnumPins::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumPins.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPins::Skip


## -description



The <code>Skip</code> method skips over a specified number of pins.




## -parameters




### -param cPins [in]

Number of pins to skip.


## -returns



Returns one of the following <b>HRESULT</b>

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped past the end of the sequence.

</td>
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
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The filter's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>
 




## -remarks



If the number of pins changes, the enumerator is no longer consistent with the filter, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://msdn.microsoft.com/c2147884-aec2-43ae-b85a-61383ad6ca15">IEnumPins::Reset</a> method. You can then call the <code>Skip</code> method safely.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/839190b4-fd29-4a94-8838-d84adfdd9668">IEnumPins Interface</a>
 

 

