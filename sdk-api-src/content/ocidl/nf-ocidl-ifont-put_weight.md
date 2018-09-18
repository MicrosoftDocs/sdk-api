---
UID: NF:ocidl.IFont.put_Weight
title: IFont::put_Weight
author: windows-sdk-content
description: Sets the font's Weight property.
old-location: com\ifont_put_weight.htm
tech.root: com
ms.assetid: 716c77f3-6224-40d7-abea-46ed5eedb08a
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IFont interface [COM],put_Weight method, IFont.put_Weight, IFont::put_Weight, _ctrl_ifont_put_weight, com.ifont_put_weight, ocidl/IFont::put_Weight, put_Weight, put_Weight method [COM], put_Weight method [COM],IFont interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.put_Weight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFont::put_Weight


## -description


Sets the font's Weight property. 


## -parameters




### -param weight [in]

The new Weight for the font. For a list of available font weights, see the description of the <b>lfWeight</b> member of 
    the <a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure.


## -returns



This method can return one of these values.

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
The Weight property was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This font does not support different weights. This value is not an error condition.

</td>
</tr>
</table>
 




## -remarks



This property may 
   affect the Bold property as well. The Bold 
   property is set to <b>TRUE</b> if the Weight property is 
   greater than the average of <b>FW_NORMAL</b> (400) and <b>FW_BOLD</b> (700), 
   that is 550.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/3dad6648-752d-48f8-9267-24a5f5b0346c">IFont::get_Weight</a>
 

 

