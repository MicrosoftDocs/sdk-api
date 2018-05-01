---
UID: NF:olectl.FONTSIZE
title: FONTSIZE macro
author: windows-driver-content
description: Gets or sets the font size.
old-location: sidebar\fontsize_property_gText.htm
old-project: sidebar
ms.assetid: VS|sidebar|~\sidebar\reference\graphicsreference\gtext\fontsize_property_gtext.htm
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: FONTSIZE, fontsize property [Windows Sidebar], fontsize property [Windows Sidebar], text object, fontsize_property_gText, sidebar.fontsize_property_gText, text object [Windows Sidebar], fontsize property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sidebar.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PARAMDATA, *LPPARAMDATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sidebar.Exe
api_name:
-	text.fontsize
product: Windows
targetos: Windows
req.lib: 
req.dll: Sidebar.Exe (version 1.00 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# FONTSIZE macro


## -description


<p class="CCE_Message">[The Windows Gadget Platform/Sidebar is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.
]

Gets or sets the font size.
		

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Important</b>  For Windows 7, when the new <code>&lt;autoscaleDPI&gt;</code> element of the gadget manifest is set to true (for high-DPI support) gadgets should explicitly specify a text size.</div>
<div> </div>

#### Examples

The following example demonstrates how to assign a font size to the <a href="https://msdn.microsoft.com/038e9fae-137d-49b2-9fbe-be7e3affc117">g:text</a> element from a gadget script file.

<div class="code"><span codelanguage="JScript"><table>
<tr>
<th>JScript</th>
</tr>
<tr>
<td>
<pre>\\ imgBackground is the value of the 'id' attribute for the g:background element.
var txtSize = imgBackground.addTextObject("test", "Verdana", 25, "Red", intX, intY);
txtSize.fontsize = 12;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/9d0467d9-a02c-4629-be60-6effb551721d">background</a>



<a href="https://msdn.microsoft.com/bcc3db81-45e8-46ae-af49-8f81829c0303">image</a>



<a href="https://msdn.microsoft.com/038e9fae-137d-49b2-9fbe-be7e3affc117">text</a>
 

 

