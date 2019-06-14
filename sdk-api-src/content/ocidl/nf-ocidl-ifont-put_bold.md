---
UID: NF:ocidl.IFont.put_Bold
title: IFont::put_Bold (ocidl.h)
author: windows-sdk-content
description: Sets the font's Bold property.
old-location: com\ifont_put_bold.htm
tech.root: com
ms.assetid: c25738fe-daf4-4eac-b4b0-354950e29f27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Bold method, IFont.put_Bold, IFont::put_Bold, _ctrl_ifont_put_bold, com.ifont_put_bold, ocidl/IFont::put_Bold, put_Bold, put_Bold method [COM], put_Bold method [COM],IFont interface
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
 - IFont.put_Bold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFont::put_Bold


## -description


Sets the font's Bold property. 


## -parameters




### -param bold [in]

The new Bold property for the font.


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
The bold state was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support a bold state. Note that this is not an error condition.

</td>
</tr>
</table>
 




## -remarks



Changing the 
   Bold property may also change the Weight 
   property. Setting the Bold property to <b>TRUE</b> sets the 
   Weight property to <b>FW_BOLD</b> (700); setting the 
   Bold property to <b>FALSE</b> sets the 
   Weight property to <b>FW_NORMAL</b> (400).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ifont-get_bold">IFont::get_Bold</a>
 

 

