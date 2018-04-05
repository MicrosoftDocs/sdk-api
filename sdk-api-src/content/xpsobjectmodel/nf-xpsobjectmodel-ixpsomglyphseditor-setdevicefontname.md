---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetDeviceFontName
title: IXpsOMGlyphsEditor::SetDeviceFontName method
author: windows-driver-content
description: Sets the name of the device font.
old-location: xps\ixpsomglyphseditor_setdevicefontname.htm
old-project: printdocs
ms.assetid: d580f768-0c6a-4799-8ad8-d6f73b9216b9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMGlyphsEditor, IXpsOMGlyphsEditor interface [XPS Documents and Packaging], SetDeviceFontName method, IXpsOMGlyphsEditor::SetDeviceFontName, SetDeviceFontName method [XPS Documents and Packaging], SetDeviceFontName method [XPS Documents and Packaging], IXpsOMGlyphsEditor interface, SetDeviceFontName,IXpsOMGlyphsEditor.SetDeviceFontName, xps.ixpsomglyphseditor_setdevicefontname, xpsobjectmodel/IXpsOMGlyphsEditor::SetDeviceFontName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMGlyphsEditor.SetDeviceFontName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGlyphsEditor::SetDeviceFontName method


## -description


Sets the name of the device font.


## -parameters




### -param deviceFontName [in]

A pointer to the string that contains the name of the device font in its unescaped form. A <b>NULL</b> pointer clears the property.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The device font name that is passed in <i>deviceFontName</i> can be set in  its unescaped form; it will be converted to its escaped form when the document is serialized.




## -see-also




<a href="https://msdn.microsoft.com/5bdf2892-ce6f-4560-b638-e441166fc309">IXpsOMGlyphsEditor</a>
 

 

