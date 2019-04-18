---
UID: NF:xpsobjectmodel.IXpsOMGlyphsEditor.SetDeviceFontName
title: IXpsOMGlyphsEditor::SetDeviceFontName (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the name of the device font.
old-location: xps\ixpsomglyphseditor_setdevicefontname.htm
tech.root: printdocs
ms.assetid: d580f768-0c6a-4799-8ad8-d6f73b9216b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphsEditor interface [XPS Documents and Packaging],SetDeviceFontName method, IXpsOMGlyphsEditor.SetDeviceFontName, IXpsOMGlyphsEditor::SetDeviceFontName, SetDeviceFontName, SetDeviceFontName method [XPS Documents and Packaging], SetDeviceFontName method [XPS Documents and Packaging],IXpsOMGlyphsEditor interface, xps.ixpsomglyphseditor_setdevicefontname, xpsobjectmodel/IXpsOMGlyphsEditor::SetDeviceFontName
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphsEditor.SetDeviceFontName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGlyphsEditor::SetDeviceFontName


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
 

 

