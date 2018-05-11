---
UID: NN:imepad.IImePadApplet
title: IImePadApplet
author: windows-driver-content
description: The IImePadApplet interface inputs strings into apps through the IImePad interface.
old-location: intl\iimepadapplet.htm
old-project: Intl
ms.assetid: F3BC7176-9659-47B6-AFCA-049807394961
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IImePadApplet, IImePadApplet interface [Internationalization for Windows Applications], IImePadApplet interface [Internationalization for Windows Applications],described, imepad/IImePadApplet, intl.iimepadapplet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imepad.h
req.include-header: 
req.target-type: Windows
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Imepad.h
api_name:
-	IImePadApplet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IImePadApplet interface


## -description


The <b>IImePadApplet</b> interface inputs strings into apps through the <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> interface.

<b>IImePadApplet</b> should be implemented as a DLL inproc server. The developer can implement multiple <b>IImePadApplet</b> interfaces in one DLL.  To specify and emulate the <b>IImePadApplet</b> interface in the applet DLL, the applet must also provide the <a href="https://msdn.microsoft.com/788C7272-3BFF-4531-B66E-211585BF85E3">IImeSpecifyApplets</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePadApplet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IImePadApplet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImePadApplet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4F79A20-E69E-4EA0-A992-4415B8AA4790">CreateUI</a>
</td>
<td align="left" width="63%">
Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to get the applet's window handle, style, and size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D24EF900-01D4-4E6E-B752-B11B2F4A6A6C">GetAppletCfg</a>
</td>
<td align="left" width="63%">
Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to get <b>IImePadApplet</b>'s configuration data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> interface to initialize <b>IImePadApplet</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C370DC8-D308-4339-81F3-FEE88359A52F">Notify</a>
</td>
<td align="left" width="63%">
Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to pass information with a notify code

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/864E5CBB-8056-46B5-BF78-9A66EC861F8A">Terminate</a>
</td>
<td align="left" width="63%">
Called from <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> to terminate <b>IImePadApplet</b> when the IMEPad instance exits.

</td>
</tr>
</table> 

