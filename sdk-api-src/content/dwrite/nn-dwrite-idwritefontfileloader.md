---
UID: NN:dwrite.IDWriteFontFileLoader
title: IDWriteFontFileLoader
author: windows-sdk-content
description: Handles loading font file resources of a particular type from a font file reference key into a font file stream object.
old-location: directwrite\IDWriteFontFileLoader.htm
tech.root: DirectWrite
ms.assetid: 855e281e-3855-4c11-af87-68f8e0dadbf8
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDWriteFontFileLoader, IDWriteFontFileLoader interface [Direct Write], IDWriteFontFileLoader interface [Direct Write],described, directwrite.IDWriteFontFileLoader, dwrite/IDWriteFontFileLoader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFileLoader interface


## -description


 Handles loading font file resources of a particular type from a font file reference key into a font file stream object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFileLoader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c0a7c7b-8201-45c5-ac46-20f0df034ccd">CreateStreamFromKey</a>
</td>
<td align="left" width="63%">
 Creates a font file stream object that encapsulates an open file resource.
     

</td>
</tr>
</table> 


## -remarks



The font file loader interface is recommended to be implemented by a singleton object. Note that font file loader implementations must not register themselves with DirectWrite factory inside their constructors and must not unregister themselves in their destructors, because registration and unregistraton operations increment and decrement the object reference count respectively. Instead, registration and unregistration of font file loaders with DirectWrite factory should be performed outside of the font file loader implementation as a separate step.



