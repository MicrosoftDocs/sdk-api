---
UID: NN:shobjidl_core.IExtractImage
title: IExtractImage
author: windows-sdk-content
description: Exposes methods that request a thumbnail image from a Shell folder.
old-location: shell\IExtractImage.htm
old-project: shell
ms.assetid: 28a13749-89e7-407e-89cb-95464859ce3e
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IExtractImage, IExtractImage interface [Windows Shell], IExtractImage interface [Windows Shell],described, _win32_IExtractImage, shell.IExtractImage, shobjidl_core/IExtractImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IExtractImage
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.70 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IExtractImage interface


## -description


Exposes methods that request a thumbnail image from a Shell folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtractImage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtractImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtractImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c40e2cf-c706-4a4a-819f-a416d6846158">Extract</a>
</td>
<td align="left" width="63%">
Requests an image from an object, such as an item in a Shell folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1113429-ea89-4650-b345-db9e275232e6">GetLocation</a>
</td>
<td align="left" width="63%">
Gets a path to the image that is to be extracted.

</td>
</tr>
</table> 


## -remarks



There are two steps in the process: First, use <a href="https://msdn.microsoft.com/f1113429-ea89-4650-b345-db9e275232e6">GetLocation</a> to request the path description of an image and specify how the image should be rendered. Then, call <a href="https://msdn.microsoft.com/7c40e2cf-c706-4a4a-819f-a416d6846158">Extract</a> to extract the image.

If the object is free-threaded it must also expose an <a href="https://msdn.microsoft.com/158a6688-949b-4075-a790-fd6efb88792c">IRunnableTask</a> interface so it can be stopped and started as needed. This feature can be particularly useful when extraction may be slow.

Implement <b>IExtractImage</b> if your namespace extension needs to provide thumbnail images to be displayed in a Shellview.

Use <b>IExtractImage</b> if you are implementing a view of namespace objects, and want to display thumbnail images. You can use a Shell folder's <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">IShellFolder::GetUIObjectOf</a> method to bind to its <b>IExtractImage</b> interface.



