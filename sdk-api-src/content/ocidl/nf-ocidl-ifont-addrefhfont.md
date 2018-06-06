---
UID: NF:ocidl.IFont.AddRefHfont
title: IFont::AddRefHfont
author: windows-sdk-content
description: Notifies the font object that the previously realized font identified with hFont should remain valid until ReleaseHfont is called or the font object itself is released completely.
old-location: com\ifont_addrefhfont.htm
old-project: com
ms.assetid: f86d52b8-e763-4948-b853-039721ae9b38
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: AddRefHfont, AddRefHfont method [COM], AddRefHfont method [COM],IFont interface, IFont interface [COM],AddRefHfont method, IFont.AddRefHfont, IFont::AddRefHfont, _ctrl_ifont_addrefhfont, com.ifont_addrefhfont, ocidl/IFont::AddRefHfont
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.AddRefHfont
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFont::AddRefHfont


## -description


Notifies the font object that the previously realized font identified with <i>hFont</i> should remain valid until <a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a> is called or the font object itself is released completely.


## -parameters




### -param hFont [in]

Font handle previously realized through <a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a> to be locked in the font object's cache.


## -returns



The method supports the standard return values <b>E_UNEXPECTED</b> and <b>E_INVALIDARG</b>, as well as the following values.

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
The font was successfully locked in the cache.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68">ReleaseHfont</a>



<a href="https://msdn.microsoft.com/19bfd78a-0e81-45c3-a3b8-bc893669e9f5">get_hFont</a>
 

 

