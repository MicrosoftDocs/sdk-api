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

# IWMPClosedCaption::put_SAMIFileName


## -description



The <b>put_SAMIFileName</b> method specifies the name of the file containing the information needed for closed captioning.




## -parameters




### -param bstrSAMIFileName [in]

<b>BSTR</b> containing the SAMI file name.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The SAMI file must use an .smi or .sami file name extension.

Once you specify a value using <b>put_SAMIFileName</b>, that value persists until you specify a new value (or until a new media item is opened by using the <i>sami</i> URL parameter). Therefore, you must specify a new value with this method before you play each new media item. The new value will take effect when the next media item is opened (or when <b>IWMPCore::close</b> is called). Specifying a new value by using <b>put_SAMIFileName</b> has no effect on the current media item.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/0fdd2cdc-32d4-4fda-9596-b050107abd5f">Adding Closed Captions to Digital Media</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/2f09df76-3bfc-48ce-881f-c905656ecbbf">IWMPClosedCaption::get_SAMIFileName</a>



<a href="https://msdn.microsoft.com/e6e21995-5dbd-4893-a9f2-6ce918d3fbc4">IWMPCore::close</a>
 

 

